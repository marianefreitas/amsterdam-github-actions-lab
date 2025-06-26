# 🚀 Guilda Pública - Squad Amsterdam  
## Tema: GitHub Actions

Bem-vindos à Guilda Pública da Squad Amsterdam! 🎉  
Este repositório contém os materiais e exemplos apresentados durante nossa sessão sobre **GitHub Actions**, uma ferramenta poderosa para automação de fluxos de trabalho no GitHub.

---

## 📄 Documentação

📥 Baixe os slides da guilda em PDF:  
👉 [Clique aqui para baixar o PDF](./docs/PDF/slidesGuildaGitHubActionsSquadAmsterdam.pdf)

---

## 🎯 Roteiro da Apresentação

1. **Introdução**  
   → *Por que GitHub Actions?*

2. **O que é GitHub Actions**  
   → *Visão geral sobre a ferramenta*

3. **Como funciona?**  
   → *Workflow, Events, Jobs, Steps, Actions, Runners*

4. **Demonstração prática**  
   → *Mão na massa*

5. **Considerações finais**  
   → *Dúvidas e curiosidades*

---

## 🧩 Introdução: Por que escolhemos esse tema?

- **GitHub é a maior plataforma de armazenamento de código**
  - Todos nós conhecemos, temos conta, temos repositórios
  - Usado em:
    - Faculdade
    - Projetos pessoais
    - Cursos
  - Ou seja, o GitHub **não é novidade**

- **A novidade é que o GitHub está chegando no BB**
  - Março de 2025: Guilda BB
  - Processo em andamento
  - Aos poucos, projetos podem ter a iniciativa de começar o processo
  - 🎥 [Link da Guilda do BB sobre a chegada do GitHub](https://oss.servicos.bb.com.br:10443/pss3devdf002/GuildaCloud/Videos/G211githubnobbumanovajornadadodev.mp4)

- **Redução da Carga Cognitiva do Dev** foi um dos objetivos apresentados pelo BB
  - Exemplo de como é hoje:
    - `commit` no GitLab → ferramenta → interface → curva de aprendizado → gerenciamento de credenciais → etc.
    - `build` no Jenkins → ferramenta → interface → curva de aprendizado → gerenciamento de credenciais → etc.
    - Processos Cloud → Plataforma → AIC → etc.
  - **Carga Cognitiva do Dev** = tudo o que nós, devs, precisamos lembrar, configurar, entender para entregar algo

- **Como vai ser possível reduzir essa carga cognitiva?**
  - Unificando os processos em um único lugar e interface
  - A ferramenta do GitHub que integra esses processos de forma eficiente é o **GitHub Actions**
  - ✨ Por esse motivo, resolvemos explorar um pouco com vocês sobre o **GitHub Actions**
 
---

## 🔍 O que é o GitHub Actions? 

- Lançado em **2018** em beta e **público em 2019**  
  → Parte do movimento do GitHub para fornecer uma *plataforma completa de DevOps*
  
- Ferramenta de **automação do desenvolvimento de software**

- Um dos principais usos é **CI/CD** (Integração e Entrega Contínuas)

- Em projetos **Open Source**, permite automatizar fluxos como:
  - Issues
  - Pull Requests  
  → Esses fluxos podem ser automatizados para facilitar o processo de desenvolvimento

 ---

 ## ⚙️ Como funciona?

### 🛠️ Workflows 
- O **workflow** é onde configuramos o fluxo de automação.
- Ele é um documento com extensão `.yml`.
- Esse documento fica dentro da estrutura: `.github/workflows/nomeArquivo.yml`.
- Ele define **QUANDO** e **COMO** os processos de automação devem acontecer.
- O nome do arquivo `.yml` pode ser definido livremente.

---

### ⏰ Events 
- Os **Eventos** são os **"QUANDOS"** definidos no arquivo `.yml`.
- Quando um evento acontece, o workflow começa a ser executado.
- Exemplos de eventos:
  - Criação de branch
  - Alterações em regras de branch
  - Atualizações em wikis
  - Criação e alteração de labels
  - Push, Pull Request, Issue
- Documentação completa de eventos:  
  🔗 [GitHub Events Reference](https://docs.github.com/en/actions/reference/events-that-trigger-workflows)
- No arquivo `.yml`, os eventos são definidos com a chave `on`.

> 💡 Exemplo visual da estrutura no `.yml`:

![Exemplo 1](attachment:c778ff5e-20a3-4b32-918e-71557d4db831:image.png)  
![Exemplo 2](attachment:90c5e801-1585-4d15-a104-767ea6539c3f:image.png)  
![Exemplo 3](attachment:409eb2e9-9ed1-4c4c-92f2-197f0a30961a:image.png)

---

### 🧩 Jobs 
- No workflow temos:
  - O **QUANDO** (Events)
  - O **COMO** (Jobs)
- Os **Jobs** são unidades completas de trabalho.
- Cada job é independente por padrão, mas pode ser executado em sequência com `needs:`.
- Os jobs podem rodar **em paralelo**.
- No arquivo `.yml`, a chave é `jobs`.

---

### 🎮 Steps 
- Um **job** é como uma **fase** de um jogo.
- Os **steps** são os passos necessários para concluir essa fase.
- No `.yml`, são definidos em `steps`.
- Tipos de step:
  - `run` → comandos shell (ex: `npm install`, `npm test`, `echo`)
  - `uses` → utiliza uma **action** externa ou personalizada

---

### 🔁 Actions 
- Um **step do tipo `uses`** utiliza uma **action**.
- **Actions** são blocos reutilizáveis para tarefas comuns ou complexas.
- Podem ser:
  - Criadas por você
  - Reutilizadas do GitHub Marketplace
- Exemplos de actions:
  - **Autenticação** → usa secrets para login seguro
  - **Configuração de ambiente** → instala ferramentas
  - **Code review automático** → linters e validações
- 🔗 [GitHub Actions Marketplace](https://github.com/marketplace?type=actions)

---

### 🖥️ Runners 
- Os **runners** são os servidores/ambientes onde os jobs e steps são executados.
- Um runner executa **um job por vez**.
- No arquivo `.yml`, são definidos com `runs-on`.
- É possível usar **matriz (`matrix`)** para testar diferentes combinações:
  - Diferentes SOs
  - Versões de dependências

---

## 🧾 Considerações Finais

- O **GitHub Actions** se destaca por sua **fácil integração** com diferentes ferramentas e serviços.
- É uma solução poderosa e acessível para **automatizar processos** do dia a dia de desenvolvimento.
- Com ele, é possível simplificar tarefas repetitivas, melhorar a confiabilidade das entregas e reduzir a carga cognitiva dos times.
- A curva de aprendizado é suave, especialmente para quem já utiliza o GitHub no dia a dia.
- Esperamos que a apresentação tenha despertado a curiosidade para explorar e aplicar o GitHub Actions nos seus projetos!

🚀 *Automatizar é libertador — e o primeiro passo pode ser simples!*


