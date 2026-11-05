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

### 🧹 [Limpeza de disco](https://github.com/JonatasAlves21/limpeza-disco)
Para chamados de "disco cheio" ou "computador lento". Primeiro o script mostra o que
está ocupando o disco, sem apagar nada. Depois limpa etapa por etapa, pedindo
confirmação em cada uma (ou sozinho, quando roda pela ferramenta de gestão das
máquinas), e no fim gera um relatório pronto para colar no chamado.
**Resultado medido:** num atendimento real, o espaço livre foi de **22,75 GB para
44,58 GB**, sem apagar nenhum documento do usuário.

`PowerShell` `System.IO` `DISM` `Windows`

### 💿 [Imagem do Windows 11 atualizada](https://github.com/JonatasAlves21/windows-imaging-toolkit)
Prepara o SSD de formatação para instalar o Windows 11 já atualizado e com driver de
rede. Assim a máquina formatada não fica sem internet nem passa horas no Windows
Update. Baixa os drivers oficiais da Dell e da Lenovo, separa os essenciais, aplica a
última atualização da Microsoft na imagem e gera a ISO nova, conferindo cada pacote
baixado.
**Resultados medidos:** ISO de **9,29 GB** já na versão de ago/2026, com 241 MB de
drivers embutidos; download dos pacotes de driver de **182 KB/s para 11,9 MB/s**
usando várias conexões em paralelo.

`PowerShell` `DISM` `oscdimg` `HTTP Range` `RunspacePool`

### 📦 [Relatório de equipamentos não devolvidos](https://github.com/JonatasAlves21/topdesk-ativos-nao-devolvidos)
Toda segunda-feira, mostra à gestão quantos notebooks e celulares de ex-colaboradores
ainda não foram devolvidos para a TI, de quais centros de custo e estados, e há
quanto tempo. Lê os dados da plataforma de service desk pela API, monta um Excel com
o resumo e publica no SharePoint. As senhas ficam num cofre de senhas, e um fluxo do
Power Automate avisa se o relatório não for atualizado.
**Resultado medido:** a execução caiu de **10min23 para 1min28** (cerca de 7× mais
rápido) depois de limitar quantas páginas do histórico de cada equipamento o script
lê.

`Node.js` `API REST` `Microsoft Graph` `ExcelJS` `Power Automate` `Cofre de senhas`

---

## Como eu trabalho

- **Medir antes e depois.** Todo script registra o estado inicial e o resultado, para
  o ganho ser um número e não uma impressão.
- **Seguro por padrão.** Diagnóstico separado da ação, confirmação explícita no que
  é irreversível, nada de credencial no código.
- **Documentar as armadilhas.** O que custou tempo vira comentário no código e seção
  no README.
