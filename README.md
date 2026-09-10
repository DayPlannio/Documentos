# DayPlannio - Aplicativo para Organização de Rotina de Autônomos

**Autores:** Alissa Gabriel e Raissa Geovana Araujo.

---

## Sumário

- [1. Introdução](#1-introdução)
  - [Objetivos](#-objetivos)
  - [Metodologia](#-metodologia)
- [2. Requisitos](#2-requisitos)
  - [Requisitos funcionais](#-requisitos-funcionais)
  - [Requisitos não funcionais](#-requisitos-não-funcionais)
- [3. Modelo de casos de uso](#3-modelo-de-casos-de-uso)
- [4. Modelo do banco de dados](#4-modelo-do-banco-de-dados)
- [5. Banco de dados](#5-banco-de-dados)
- [6. Diagrama de classes](#6-diagrama-de-classes)
- [7. Estudo de viabilidade](#7-estudo-de-viabilidade)
- [8. Regras de negócio (Modelo canvas)](#8-regras-de-negócio-modelo-canvas)
- [9. Design](#9-design)
- [10. Protótipo](#10-protótipo)
- [11. Aplicação](#11-aplicação)
- [12. Considerações finais](#12-considerações-finais)
- [13. Referências](#13-referências)

---

# 1. Introdução

No cenário atual, a organização da rotina e a gestão eficiente do tempo têm se tornado cada vez mais importantes para profissionais autônomos que precisam lidar diariamente com múltiplas tarefas, clientes e serviços. A falta de uma solução que centralize agenda, cadastro de clientes, controle financeiro e gestão de serviços em um único ambiente dificulta a administração das atividades profissionais.

O DayPlannio surge para suprir essa necessidade, oferecendo uma plataforma integrada composta por aplicativo mobile, portal web e serviços em nuvem. A solução permite organizar compromissos, acompanhar atendimentos, registrar clientes, controlar ganhos e despesas, além de disponibilizar métricas de produtividade, faturamento, tempo trabalhado e desempenho dos atendimentos.

A plataforma também contará com recursos de Internet das Coisas (IoT) e mineração de dados para automatizar a coleta e análise de informações, permitindo a geração de métricas e relatórios gerenciais. Além disso, os clientes poderão acompanhar o histórico de serviços realizados por meio do portal web, enquanto os prestadores poderão divulgar seus trabalhos em um portfólio público com fotos dos atendimentos, mediante autorização prévia. Os dados e imagens da plataforma serão armazenados em nuvem, garantindo sua disponibilidade e integração entre os diferentes módulos do sistema.

## • Objetivos

### Objetivo Geral

Desenvolver a plataforma DayPlannio para auxiliar profissionais autônomos na organização de sua rotina, integrando agenda de serviços, cadastro de clientes, controle financeiro, acompanhamento de atendimentos, métricas de desempenho e recursos de Internet das Coisas (IoT) para automatização de registros operacionais. A solução contará com aplicativo mobile para gestão das atividades do prestador, portal web para clientes acompanharem métricas e histórico de serviços realizados, portal administrativo para gerenciamento de clientes, prestadores e registros do sistema, além de uma área pública para divulgação dos serviços realizados por meio de um portfólio contendo fotos dos atendimentos, disponibilizadas mediante autorização do prestador. Dessa forma, todas as informações serão reunidas em um único ambiente digital, proporcionando uma gestão centralizada e eficiente das atividades profissionais.

A proposta busca proporcionar maior organização, produtividade e controle das atividades profissionais, oferecendo também recursos para acompanhamento dos serviços pelos clientes.

### Objetivos Específicos

**Pesquisar Outras Aplicações de Gestão e Produtividade**
Analisar sistemas existentes de organização, agenda e gestão de atividades para identificar boas práticas e funcionalidades relevantes, como visualização de dados, integração com calendários, controle financeiro, acompanhamento de métricas, histórico de serviços, portais web e recursos de geolocalização, garantindo que o DayPlannio ofereça uma experiência moderna, eficiente e alinhada às necessidades dos usuários.

**Identificar ferramentas**
Definir os requisitos técnicos e funcionais da aplicação, considerando aspectos como desenvolvimento front-end, back-end, banco de dados, segurança, escalabilidade, geolocalização, Internet das Coisas (IoT), mineração de dados, computação em nuvem e manutenção, para assegurar que o desenvolvimento da aplicação seja eficiente, seguro e escalável.

## • Metodologia

Para o desenvolvimento da plataforma DayPlannio, foram adotadas ferramentas e tecnologias atuais que contribuem para a construção de um sistema eficiente, seguro e de fácil manutenção. A escolha dessas tecnologias visa otimizar o processo de desenvolvimento e garantir a integração entre os módulos mobile, web, nuvem, IoT e mineração de dados da aplicação. Dentre as ferramentas utilizadas, estão:

- **Linguagens de Programação:** C#, responsável pela implementação da lógica de negócio da aplicação, APIs, funcionalidades do aplicativo mobile e dos portais web. Linguagem moderna, orientada a objetos e amplamente utilizada na plataforma .NET.
- **Frameworks e Bibliotecas:**
  - **.NET MAUI** — desenvolvimento mobile multiplataforma (Android e iOS) a partir de uma única base de código.
  - **ASP.NET** — construção das APIs responsáveis pela comunicação entre aplicação, banco de dados e serviços web.
  - **ASP.NET MVC** — portais web para clientes, administradores e portfólio público dos prestadores.
- **Internet das Coisas (IoT):** recursos de geolocalização (geofencing) para identificar automaticamente a chegada e saída do prestador de serviço, registrando essas informações sem interação manual do usuário.
- **Mineração de Dados:** coleta, organização e análise das informações geradas pelos atendimentos, gerando métricas de produtividade, faturamento, tempo trabalhado e desempenho, disponibilizadas nos dashboards do sistema.
- **Banco de Dados:** MongoDB, sistema não relacional orientado a documentos (JSON/BSON), com alta flexibilidade, bom desempenho e escalabilidade horizontal.
- **Computação em Nuvem:** Microsoft Azure em conjunto com MongoDB Atlas, para armazenamento e processamento de dados, métricas e imagens do portfólio, garantindo disponibilidade, escalabilidade e segurança.
- **Qualidade e Testes de Software:** aplicação de conceitos, normas e modelos de qualidade de processo e produto, verificação e validação de software, e técnicas de teste para identificação de falhas e melhoria contínua.
- **Ferramentas de Controle de Versão:** Git e GitHub, para versionamento do código-fonte, rastreabilidade das modificações e colaboração da equipe.
- **Modelo de Processo de Desenvolvimento:** Kanban, organizando o fluxo de trabalho em colunas ("A Fazer", "Em Andamento", "Concluído").
- **Prototipagem:** Figma, para validar conceitos e interações do usuário antes do desenvolvimento completo.
- **Cronograma do Projeto:** Trello, para gestão visual do cronograma e acompanhamento das tarefas.
  Link do cronograma: <https://trello.com/invite/b/69a978e1ea6fcdc0da80330f/ATTId141e10f85548ec9e1e46c60d1084b05A0FC1CB9/dayplannio>

---

# 2. Requisitos

Um documento de requisitos de sistema é uma peça-chave no desenvolvimento de software, especialmente em contextos acadêmicos e profissionais. Ele consiste em um registro detalhado e estruturado dos requisitos que o sistema deve atender para alcançar seus objetivos, descrevendo tanto os requisitos funcionais quanto os não funcionais, servindo como um contrato entre os stakeholders do projeto.

## • Requisitos funcionais

Requisitos funcionais são as especificações detalhadas das funcionalidades que um sistema deve oferecer para atender às necessidades dos usuários, descrevendo as ações que o sistema deve ser capaz de realizar.

| ID | Requisito | Descrição |
|----|-----------|-----------|
| RF1 | Criar Agendamento | Permitir que o usuário cadastrado registre novos serviços em sua agenda, informando cliente, tipo de serviço, data, hora, observações, valor cobrado e custo material. |
| RF2 | Editar Agendamento | Permitir que o usuário altere detalhes de um serviço previamente agendado. |
| RF3 | Cancelar Agendamento | Permitir que o usuário cancele um serviço previamente agendado. |
| RF4 | Concluir Agendamento | Permitir que o usuário conclua um serviço. |
| RF5 | Visualizar Agenda | Permitir que o usuário visualize sua agenda em diferentes modos: diária, semanal e mensal. |
| RF6 | Cadastrar Usuário | Permitir que novos usuários se cadastrem fornecendo nome completo, e-mail, senha, confirmação de senha e telefone. |
| RF7 | Realizar Login | Permitir que usuários acessem o sistema informando e-mail e senha. |
| RF8 | Recuperar Senha | Permitir que usuários solicitem a redefinição de senha através do e-mail cadastrado. |
| RF9 | Exibir Informações do Perfil | Permitir que o usuário visualize seus dados pessoais cadastrados. |
| RF10 | Editar Informações do Perfil | Permitir que o usuário atualize seus dados pessoais, garantindo que as informações estejam sempre corretas. |
| RF11 | Cadastrar Cliente | Permitir que o usuário adicione clientes com informações básicas: nome, telefone, endereço e observações. |
| RF12 | Listar Clientes | Permitir que usuários visualizem seus clientes cadastrados. |
| RF13 | Editar Cliente | Permitir que usuários editem seus clientes cadastrados. |
| RF14 | Histórico de Cliente | Permitir que usuários visualizem os históricos de serviço por cliente. |
| RF15 | Cadastrar Tipo do Serviço | Permitir que o usuário registre serviços oferecidos, informando tipo, descrição e tempo estimado. |
| RF16 | Listar Tipo de Serviço | Permitir que o usuário visualize os serviços cadastrados. |
| RF17 | Editar Tipo de Serviço | Permitir que usuários editem seus serviços cadastrados. |
| RF18 | Excluir Tipo de Serviço | Permitir que usuários excluam seus serviços cadastrados. |
| RF19 | Registrar Entradas e Saídas | Permitir que o usuário registre tipo (entrada/saída), descrição, valor, data e categoria. |
| RF20 | Editar Registro Financeiro | Permitir que usuários editem seus registros financeiros cadastrados. |
| RF21 | Excluir Registro Financeiro | Permitir que usuários excluam seus registros financeiros cadastrados. |
| RF22 | Calcular Lucros | Calcular automaticamente lucro bruto e lucro líquido com base nos agendamentos concluídos em modo diário, semanal ou mensal. |
| RF23 | Calcular Lucros Geral | Calcular automaticamente lucro bruto e lucro líquido com base nos agendamentos concluídos e registros financeiros avulsos em modo diário, semanal ou mensal. |
| RF24 | Gerar Relatórios Financeiros | Gerar relatórios diários, semanais e mensais, com filtro por período, podendo exportar em PDF. |

## • Requisitos não funcionais

Os requisitos não funcionais referem-se às características e restrições do sistema que não estão diretamente relacionadas às suas funcionalidades principais, mas que são essenciais para garantir sua qualidade, desempenho e usabilidade.

- **RNF1 — Desempenho:** a aplicação deve ter carregamento rápido, mesmo em conexões de internet mais lentas, para garantir uma boa experiência de usuário.
- **RNF2 — Usabilidade:** a interface da aplicação deve ser intuitiva e fácil de usar, com navegação clara e design responsivo, para que os usuários possam encontrar facilmente as informações de interesse.
- **RNF3 — Manutenibilidade:** o código-fonte da aplicação deve ser bem documentado, seguindo padrões de codificação e boas práticas de desenvolvimento, para facilitar a manutenção e futuras atualizações do sistema.

---

# 3. Modelo de casos de uso

**Figura 1 – Diagrama de Caso de Uso**
*Ver no documento word*
Fonte: Elaborado pelos autores (2026).

### Casos de Uso de Alto Nível

| Caso de Uso | Descrição |
|---|---|
| Gerenciar usuários | O usuário pode se cadastrar, editar seus dados e realizar login no sistema. |
| Gerenciar Agendamento | O usuário cadastrado pode criar, editar, cancelar e visualizar agendamentos de serviços. |
| Gerenciar Clientes | O usuário cadastrado pode cadastrar clientes, registrar histórico de serviços e adicionar observações. |
| Gerenciar Tipo de Serviço | O usuário cadastrado pode cadastrar, editar e consultar serviços, incluindo tipo, descrição e tempo estimado. |
| Controle Financeiro | O usuário cadastrado pode registrar tipo (entradas ou saídas), descrição, valor, data e categoria. |

### Casos de Uso Detalhados

<details>
<summary><b>Gerenciar Usuários</b></summary>

**Ator:** Usuário

**Pré-condições:** o sistema está disponível; o usuário não possui cadastro (fluxo de criação) ou já possui cadastro (login/edição).

**Fluxo Principal:**
1. **Cadastro** — o usuário preenche nome, e-mail, senha e telefone e clica em "Cadastrar".
2. **Login** — após o cadastro, o usuário informa e-mail e senha e é autenticado.
3. **Edição de Perfil** — o usuário atualiza seus dados e clica em "Salvar".

**Fluxos Alternativos:**
- Campos obrigatórios não preenchidos → o sistema exibe alerta e o usuário corrige ou cancela.
- Informações em formato incorreto (ex.: e-mail sem "@", senha curta) → o sistema rejeita e exibe alerta.
- Recuperação de senha via "Esqueci minha senha" → o sistema envia link de redefinição.

**Pós-condições:** usuário com conta ativa e autenticada, dados salvos e disponíveis, acesso liberado às funcionalidades do sistema.
</details>

<details>
<summary><b>Gerenciar Agendamento</b></summary>

**Ator:** Usuário Cadastrado

**Pré-condições:** usuário autenticado, com clientes e serviços cadastrados.

**Fluxo Principal:**
1. **Criar Agendamento** — seleciona cliente, tipo de serviço, data, hora, observações, valor cobrado e custo material, e salva.
2. **Visualizar Agenda** — em modo diário, semanal ou mensal.

**Fluxos Alternativos:**
- Campos obrigatórios não preenchidos.
- Dados inválidos (horário/data).
- Conflito de agendamento no mesmo horário.

**Pós-condições:** agendamento registrado e exibido corretamente; em caso de erro, nenhuma alteração é feita.
</details>

<details>
<summary><b>Gerenciar Clientes</b></summary>

**Ator:** Usuário Cadastrado

**Pré-condições:** usuário autenticado.

**Fluxo Principal:**
1. **Cadastrar Cliente** — nome, telefone, endereço e observações.
2. **Registrar Histórico de Serviços** — por cliente.

**Fluxos Alternativos:** campos não preenchidos; informações inválidas.

**Pós-condições:** cliente cadastrado com histórico; informações disponíveis para agendamentos e relatórios.
</details>

<details>
<summary><b>Gerenciar Tipo de Serviço</b></summary>

**Ator:** Usuário Cadastrado

**Pré-condições:** usuário autenticado.

**Fluxo Principal:**
1. **Cadastrar Serviço** — tipo, descrição e tempo estimado.
2. **Visualizar/Editar Serviço**.

**Fluxos Alternativos:** campos não preenchidos; valores inválidos.

**Pós-condições:** serviço cadastrado e disponível para agendamentos e relatórios.
</details>

<details>
<summary><b>Controle Financeiro</b></summary>

**Ator:** Usuário Cadastrado

**Pré-condições:** usuário autenticado.

**Fluxo Principal:**
1. **Registrar Entradas e Saídas** — tipo, descrição, valor, data e categoria.
2. **Cálculo Automático de Lucros** — lucro bruto e líquido.
3. **Gerar Relatórios Financeiros** — por período, exportáveis em PDF.

**Fluxos Alternativos:** dados incompletos.

**Pós-condições:** entradas, saídas e lucros armazenados; relatórios exportáveis em PDF.
</details>

---

# 4. Modelo do banco de dados

*(Modelo conceitual, lógico e físico)*

---

# 5. Banco de dados

O banco de dados utilizado na plataforma DayPlannio é o **MongoDB**, um sistema de gerenciamento de banco de dados não relacional orientado a documentos. Essa tecnologia foi escolhida por sua flexibilidade na modelagem dos dados, permitindo armazenar e gerenciar informações de forma eficiente e adaptável às necessidades da aplicação.

Os dados são organizados em coleções compostas por documentos no formato BSON (Binary JSON), possibilitando o armazenamento de informações relacionadas a usuários, clientes, prestadores, atendimentos, agendamentos, métricas, portfólios e demais funcionalidades da plataforma.

Além das informações operacionais, o banco de dados também armazenará os dados necessários para a geração de métricas, indicadores e relatórios gerenciais, apoiando os processos de mineração de dados da aplicação. As informações armazenadas serão compartilhadas entre o aplicativo mobile, os portais web e os demais serviços que compõem a plataforma.

A utilização do MongoDB proporciona flexibilidade, escalabilidade e bom desempenho no gerenciamento dos dados, contribuindo para a integração e o funcionamento eficiente dos diferentes módulos do sistema.

---

# 6. Diagrama de classes

O MongoDB não utiliza um Diagrama de Classe, pois é um banco de dados não relacional orientado a documentos. Em vez de organizar os dados em tabelas com relações rígidas, o MongoDB armazena informações em coleções de documentos no formato JSON (ou BSON), permitindo maior flexibilidade na modelagem dos dados.

---

# 7. Estudo de viabilidade

O estudo de viabilidade tem como objetivo analisar os aspectos técnicos, econômicos, operacionais, legais e de mercado envolvidos no desenvolvimento da aplicação web. Essa análise permite avaliar se o projeto é viável em termos de recursos disponíveis, demanda e alinhamento com os objetivos propostos.

### Viabilidade de Mercado

- **Demanda Identificada:** o crescimento do trabalho autônomo e informal no Brasil cresce cada vez mais, e muitos profissionais não têm controle total dos serviços realizados por organizarem essas informações manualmente.
- **Concorrência:** poucos aplicativos de gerenciamento de serviços para autônomos, em geral pagos e com interfaces mais complexas.
- **Diferenciais:** foco total nas necessidades de quem trabalha por conta própria, sistema de fácil aprendizado.
- **Clientes Potenciais:** trabalhadores autônomos da região.

### Viabilidade Técnica

- **Recursos Humanos:** execução conduzida pelos próprios alunos, autores do trabalho.
- **Ferramentas:** C# (linguagem), ASP.NET (backend/API), .NET MAUI (frontend mobile multiplataforma), MongoDB (banco de dados), Git e GitHub (versionamento).
- **Infraestrutura tecnológica:** computadores e conexão à internet disponibilizados pela FATEC-JAHU.
- Recursos financeiros não foram levantados, pois o projeto possui foco educacional.

### Viabilidade Operacional

- **Fluxo de Trabalho Simplificado:** foco apenas em informações essenciais para o gerenciamento pelo usuário.
- **Acessibilidade e Usabilidade:** interface intuitiva, reduzindo problemas de entendimento do sistema.
- **Geração de Lucros e valores imediatos:** o sistema registra automaticamente os valores inseridos no cálculo do lucro final.

### Viabilidade Econômica

- **Investimento inicial:** desenvolvimento, teste, validação e publicação do aplicativo, custos com ferramentas pagas.
- **Custos recorrentes:** infraestrutura (hospedagem), atualização, manutenção e divulgação do produto.
- **Benefícios Financeiros:** melhor controle financeiro, visualização clara de lucros e despesas, maior organização e produtividade.

### Conclusão do Estudo de Viabilidade

Após a análise dos aspectos de mercado, técnicos, operacionais e econômicos, conclui-se que o projeto é **viável e coerente com seus objetivos**. As tecnologias escolhidas são compatíveis com os recursos disponíveis, a aplicação é de fácil operação, e a proposta atende a uma necessidade real de organização da rotina de profissionais autônomos. Portanto, o projeto demonstra potencial para ser implementado e aprimorado futuramente.

---

# 8. Regras de negócio (Modelo canvas)

Para a elaboração do modelo de negócio, foi utilizado o **Modelo de Negócio Canvas**, permitindo planejar de forma concisa e visual os principais aspectos da aplicação web, como público-alvo, proposta de valor, canais de distribuição, fontes de receita e estrutura de custos.

**Figura 2 – Modelo de Negócio Canvas**
Fonte: Elaborado pelos autores (2026).

### O que será elaborado?

**Proposta de valor:** um aplicativo com interface intuitiva, permitindo que qualquer pessoa utilize sem necessitar de muito aprendizado sobre a plataforma, substituindo o trabalho manual do usuário por um gerenciamento automático e simplificado.

### Como será elaborado?

- **Parcerias principais:** trabalhadores autônomos.
- **Atividades principais:** gerenciar os registros de serviços realizados no dia, controlar o fluxo de caixa e a gestão de clientes.
- **Recursos principais:** equipe de desenvolvimento, internet, plataforma de hospedagem e conteúdo/informações.

### Para quem será elaborado?

- **Relacionamento com clientes:** projeto desenvolvido junto ao usuário final, com suporte humanizado e aprendizado prático.
- **Canais:** aplicativo, parcerias locais e recomendações pessoais.
- **Segmento de clientes:** autônomos locais que não possuem meios automáticos de gerenciar seus serviços.

### Quanto vai custar?

- **Estrutura de custo:** desenvolvimento e uso de ferramentas, infraestrutura (servidores, banco de dados, nuvem), manutenção, suporte, publicação e divulgação.
- **Fontes de receita:** assinaturas mensais, com plano Premium oferecendo experiência sem anúncios e recursos adicionais como exportação de relatórios em PDF.

---

# 9. Design

O design do DayPlannio é centrado na experiência do usuário, com uma interface limpa, intuitiva e organizada que facilita o gerenciamento da rotina de profissionais autônomos.

### Paleta de cores

**Figura 3 – Paleta de Cores**

A paleta de cores do DayPlannio foi cuidadosamente selecionada para transmitir organização, produtividade, simplicidade e confiança, refletindo o propósito da aplicação de auxiliar profissionais autônomos na gestão de sua rotina de forma prática e eficiente.
Fonte: Elaborado pelos autores (2026).

### Tipografia

A tipografia é um aspecto fundamental do design do DayPlannio, pois influencia diretamente a legibilidade, a estética e a experiência do usuário. Foi escolhida a fonte **Open Sans**, reconhecida por sua clareza, modernidade e versatilidade.

**Figura 4 – Exemplo Fonte Open Sans**
Fonte: Adobe (2026).

### Isotipo

O isotipo escolhido para o DayPlannio desempenha um papel importante na representação visual da aplicação e na comunicação de sua identidade voltada à organização, produtividade e gestão de atividades, buscando transmitir a ideia de planejamento, controle da rotina e praticidade no dia a dia dos profissionais autônomos.

**Figura 5 – Isotipo**
Fonte: Elaborado pelos autores (2026).

### Wireframes

Os wireframes foram desenvolvidos com o objetivo de definir a estrutura inicial das telas da aplicação, permitindo visualizar a disposição dos elementos e o fluxo de navegação antes da implementação visual definitiva.

### Modelo de navegação

O modelo de navegação da plataforma DayPlannio foi projetado para proporcionar uma experiência intuitiva e organizada aos diferentes perfis de usuários do sistema, estruturada de acordo com as funcionalidades disponíveis para cada tipo de acesso.

---

# 10. Protótipo

Foi utilizado o **Figma** na elaboração do protótipo, visando gerar uma representação visual interativa da interface da aplicação web, permitindo aos stakeholders testarem e aprimorarem o conceito antes da implementação final.

Link do protótipo: <https://www.figma.com/design/RR434kEsmEtgwjU8zBkahQ/DayPlannio?node-id=0-1&t=JTmqGH7lg5nEMBKP-1>

---

# 11. Aplicação

A seguir são apresentadas algumas telas elaboradas no sistema:

- Cadastro de Usuário
- Login de Usuário
- Redefinição de Senha / Confirmar Código / Nova Senha
- Agendamentos (visualizar, cadastrar, editar, concluir, cancelar, excluir)
- Clientes (listar, cadastrar, editar, excluir, histórico)
- Serviços (listar, cadastrar, editar, excluir)
- Entradas e Saídas (cadastrar, editar, excluir)
- Movimentações (diárias, semanais, mensais)
- Resumos (diários, semanais, mensais)
- Editar Perfil

---

# 12. Considerações finais

O desenvolvimento deste projeto contribuiu para o aprimoramento das habilidades da equipe em planejamento, trabalho em equipe e resolução de problemas durante o processo de desenvolvimento. Além disso, a aplicação oferece suporte aos trabalhadores autônomos, auxiliando na organização de suas atividades e no controle financeiro, tornando a rotina de trabalho mais prática, eficiente e organizada.

---

# 13. Referências

- ADOBE. **Open Sans.** Disponível em: <https://fonts.adobe.com/fonts/open-sans>. Acesso em: 15 abr. 2026.
- CANVA. **Canva**. Disponível em: <https://www.canva.com/pt_br/>. Acesso em: mar. 2026.
- FIGMA. **Figma**. Disponível em: <https://www.figma.com>. Acesso em: abr. 2026.
- LUCIDCHART. **LucidChart**. Disponível em: <https://www.lucidchart.com>. Acesso em: abr. 2026.
- MICROSOFT. **Visual Studio**. Disponível em: <https://visualstudio.microsoft.com>. Acesso em: abr. 2026.
- MONGODB, Inc. **MongoDB**. Disponível em: <https://www.mongodb.com>. Acesso em: abr. 2026.
- GITHUB. **GitHub**. Disponível em: <https://github.com>. Acesso em: abr. 2026.
- TRELLO. **Trello**. Disponível em: <https://trello.com/pt-BR>. Acesso em: abr. 2026.
