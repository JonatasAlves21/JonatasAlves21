# Olá, eu sou o Jonatas 👋

Trabalho com **automação e integração de sistemas** a partir do suporte de TI:
pego tarefas repetitivas do dia a dia — formatação de máquinas, limpeza de disco,
abertura e resolução de chamados, renovação de credenciais de API — e transformo em
scripts e fluxos que rodam sozinhos, com log e resultado medido.

- 🔧 **Stack:** Node.js · PowerShell · Power Automate · APIs REST · Python (em estudo)
- 🎯 **Foco:** automação de processos, integrações entre sistemas e agentes de IA
  aplicados a operações de TI
- 📍 Brasil
- 💼 [LinkedIn](https://www.linkedin.com/in/jonatasalves21)

---

## Projetos em destaque

### 🧹 [limpeza-disco](https://github.com/JonatasAlves21/limpeza-disco)
Script PowerShell para chamados de "disco cheio / computador lento". Diagnostica em
modo somente leitura, limpa com confirmação etapa a etapa (ou em modo automático para
MDM) e gera log, JSON, CSV e um HTML pronto para o chamado.
**Resultado medido:** espaço livre de **22,75 GB → 44,58 GB** em atendimento real,
sem apagar documentos do usuário.

`PowerShell` `System.IO` `DISM` `Windows`

### 💿 [windows-imaging-toolkit](https://github.com/JonatasAlves21/windows-imaging-toolkit)
Transforma um SSD Ventoy em drive de formatação que já instala o Windows 11
atualizado e com driver de rede: baixa driver packs oficiais Dell/Lenovo, filtra os
críticos, aplica o cumulative update do Microsoft Update Catalog e remonta a ISO.
Pacotes conferidos por SHA1 e área de trabalho restrita a administradores.
**Resultados medidos:** ISO de **9,29 GB** já na build de ago/2026 com 241 MB de
drivers embutidos; download de driver pack de **182 KB/s → 11,9 MB/s** com faixas
HTTP Range paralelas.

`PowerShell` `DISM` `oscdimg` `HTTP Range` `RunspacePool`

### 📦 [topdesk-ativos-nao-devolvidos](https://github.com/JonatasAlves21/topdesk-ativos-nao-devolvidos)
Relatório semanal de equipamentos não devolvidos a partir da API do TOPdesk. Recupera
pelo histórico de cada ativo a data da mudança de status e o último centro de custo,
gera um Excel com resumo executivo e o publica no SharePoint via Microsoft Graph, com
os segredos injetados pelo 1Password CLI. Um watchdog no Power Automate avisa quando
o relatório não é atualizado.
**Resultado medido:** a execução caiu de **10min23 para 1min28** (~7×) com um teto
na varredura do histórico de cada ativo.

`Node.js` `API REST` `Microsoft Graph` `ExcelJS` `Power Automate` `1Password CLI`

---

## Como eu trabalho

- **Medir antes e depois.** Todo script registra o estado inicial e o resultado, para
  o ganho ser um número e não uma impressão.
- **Seguro por padrão.** Diagnóstico separado da ação, confirmação explícita no que
  é irreversível, nada de credencial no código.
- **Documentar as armadilhas.** O que custou tempo vira comentário no código e seção
  no README.
