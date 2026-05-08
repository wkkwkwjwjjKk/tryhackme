Write-up: SOC L1 Alert Triage - TryHackMe
Introdução
Este relatório descreve a triagem de alertas realizada como Analista SOC Level 1. O principal objetivo foi aplicar priorização correta, análise contextual e tomada de decisão entre True Positive e False Positive.

Priorização dos Alertas
Segui o princípio fundamental de um SOC: priorizar pela severidade (Critical → High → Medium).

1ª Prioridade (Critical): Potential Data Exfiltration
2ª Prioridade (High): Double-Extension File Creation
3ª Prioridade (Medium): Download from GitHub Repository


Análise Detalhada e Raciocínio
1. Potential Data Exfiltration (Critical)
Verdict: False Positive
Raciocínio:
Embora o volume de dados transferidos fosse alto (~5 GB), o tráfego tinha como destino domínios da Zoom (*.zoom.us). O dispositivo envolvido estava localizado em uma sala de reunião. Este padrão é consistente com o uso normal de videochamadas corporativas (vídeo em alta qualidade, compartilhamento de tela e áudio). Não foram encontrados indicadores de exfiltração para destinos suspeitos ou IPs externos desconhecidos.
Conclusão: Comportamento legítimo da empresa.

2. Double-Extension File Creation (High)
Verdict: True Positive
Raciocínio:
Foi detectada a criação de um arquivo com dupla extensão (exemplo: document.pdf.exe). Essa é uma técnica clássica de engenharia social utilizada por malware para enganar o usuário, que muitas vezes tem a exibição de extensões desativada no Windows. Arquivos com essa característica representam alto risco de execução de código malicioso.
Conclusão: Indicador claro de possível malware. Necessita de investigação e remediação imediata.

3. Download from GitHub Repository (Medium)
Verdict: False Positive
Raciocínio:
O download foi realizado de um repositório público do GitHub (provavelmente relacionado a bibliotecas como React ou similares). Desenvolvedores baixam repositórios regularmente para trabalhar em projetos. Não havia indícios de repositórios comprometidos, links encurtados ou domínios suspeitos.
Conclusão: Atividade normal dentro do contexto de uma equipe de desenvolvimento.

Lições Aprendidas

O contexto é mais importante que o título do alerta.
Nem todo alerta de “alta gravidade” é malicioso (ex: Zoom).
Double Extension é um forte indicador de malícia.
Sempre analisar: destino, volume, usuário, dispositivo e comportamento esperado.
Seguir rigorosamente o fluxo (Assign → In Progress → Verdict → Comment → Closed) é essencial para registrar corretamente a triagem.


Bandeiras obtidas:

THM{looks_like_lots_of_zoom_meetings}
THM{how_could_this_user_fall_for_it?}
THM{should_we_allow_github_for_devs?}
