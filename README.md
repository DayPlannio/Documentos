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
| RF5 | Visualizar Agenda | Permitir que o usuário visualize sua agenda. |
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
| RF25 | Realizar Login Administrativo | Permitir que um administrador do sistema faça login pelo portal Web, separado dos usuários/prestadores comuns. |
| RF26 | Visualizar Logs do Sistema | Permitir que o administrador visualize, pelo portal Web, um histórico paginado de logs/ações realizadas no sistema. |
| RF27 | Listar Clientes (Admin) | Permitir que o administrador visualize, pelo portal Web, todos os clientes cadastrados na base, de todos os prestadores. |
| RF28 | Listar Prestadores (Admin) | Permitir que o administrador visualize, pelo portal Web, todos os prestadores (usuários) cadastrados no sistema. |
| RF29 | Gerar Credenciais do Cliente | Permitir que o prestador, ao cadastrar um cliente no app, gere automaticamente um e-mail de acesso e uma senha provisória para esse cliente. |
| RF30 | Realizar Login do Cliente | Permitir que o cliente faça login pelo portal Web utilizando o e-mail e a senha provisória gerados pelo prestador. |
| RF31 | Trocar Senha no Primeiro Acesso | Obrigar que o cliente troque a senha provisória por uma senha própria no primeiro acesso ao portal Web. |
| RF32 | Definir E-mail Secundário do Cliente | Permitir que o cliente cadastre um e-mail secundário associado ao seu perfil, pelo portal Web. |
| RF33 | Recuperar Senha do Cliente | Permitir que o cliente solicite e realize redefinição de senha pelo portal Web. |
| RF34 | Exibir Perfil do Cliente | Permitir que o cliente visualize os próprios dados de perfil pelo portal Web. |
| RF35 | Fazer Upload de Fotos de Serviço | Permitir que o prestador anexe fotos a um agendamento realizado, podendo marcá-las como públicas ou privadas. |
| RF36 | Excluir Foto | Permitir que o prestador exclua fotos cadastradas. |
| RF37 | Exibir Portfólio Público | Disponibilizar, no portal Web, uma página pública de portfólio (marketing/divulgação) com fotos marcadas como públicas, visível sem necessidade de login. |
| RF38 | Exibir Métricas de Serviço para o Cliente | Permitir que o cliente tenha acesso a métricas sobre os serviços realizados pelo prestador, como últimos serviços, média de tempo por serviço, entre outras. |
| RF39 | Exibir Métricas de Serviço para o Prestador | Permitir que o prestador tenha acesso a métricas dos próprios serviços, como ganho por tipo de serviço, média de valor por serviço, entre outras. |
| RF40 | Monitorar Presença por Geocodificação e Geofencing (Status) | Permitir converter o endereço do agendamento em latitude/longitude e monitorar a presença do prestador por geofencing. O prestador define um raio de 50m, 100m, 200m ou 500m, e o aplicativo envia a localização a cada 30 segundos. O sistema atualiza automaticamente os status: Agendado (atendimento criado), Em Atendimento (prestador dentro do raio), Em Pausa (prestador fora do raio por até 30 minutos) e Concluído (prestador fora do raio por 30 minutos, sem retorno ou outro atendimento autorizado). |
| RF41 | Definir Visibilidade do Telefone | Permitir que o prestador cadastre seu telefone de contato e defina se ele será exibido publicamente (ex.: no portfólio público) ou mantido privado, visível apenas para o próprio prestador. |
| RF42 | Autorizar Foto no Portfólio | Permitir que o administrador aprove ou recuse a foto de atendimento enviada pelo prestador. |
| RF43 | Definir Visibilidade da Cidade | Permitir que o prestador cadastre sua cidade e defina se ela será exibida publicamente (ex.: no portfólio público) ou mantida privada, visível apenas para o próprio prestador. |
| RF44 | Exibir Planos Disponíveis | Permitir que o prestador visualize os planos de assinatura (Básico, Profissional e Full), com o valor mensal e as funcionalidades incluídas em cada um. |
| RF45 | Assinar Plano | Permitir que o prestador escolha e solicite a assinatura de um dos planos disponíveis: Básico (R$ 9,90), Profissional (R$ 19,90) ou Full (R$ 29,90), ficando a ativação sujeita à aprovação do administrador. |
| RF46 | Alterar Plano | Permitir que o prestador solicite upgrade ou downgrade do plano contratado, ficando a alteração sujeita à aprovação do administrador. |
| RF47 | Cancelar Assinatura | Permitir que o prestador cancele a assinatura do plano contratado. |
| RF48 | Controlar Acesso às Funcionalidades por Plano | Liberar ou bloquear automaticamente as funcionalidades conforme o plano aprovado do prestador: Básico (agendamentos, agenda, clientes, histórico, tipos de serviço e perfil), Profissional (tudo do Básico, além de financeiro e métricas do prestador) e Full (tudo do Profissional, além de portfólio público, fotos, área e métricas do cliente e geofencing). |
| RF49 | Gerenciar Período de Teste Gratuito | Conceder a novos usuários 7 dias gratuitos no plano Full e, ao término do período, solicitar a escolha de um plano. |
| RF50 | Aprovar ou Recusar Assinatura de Plano | Permitir que o administrador visualize, pelo portal Web, as solicitações de assinatura ou alteração de plano enviadas pelos prestadores e aprove ou recuse cada uma delas. O plano só é ativado após a aprovação. |
| RF51 | Exibir Política de Privacidade | Exibir a Política de Privacidade no aplicativo mobile do prestador e no portal Web do cliente, com as seções: sobre a política, dados que coletamos, uso da localização, como usamos os dados, compartilhamento de dados, armazenamento e segurança, direitos do usuário e contato, informando a data da última atualização. |
| RF52 | Exigir Concordância no Cadastro | Exigir que o usuário leia e concorde com a Política de Privacidade para concluir o cadastro. As opções "Concordar" e "Não concordar" só são liberadas depois que o usuário rola a política até o final. Sem a concordância, a conta não é criada. |
| RF53 | Reler a Política de Privacidade | Permitir que o usuário acesse e releia a Política de Privacidade a qualquer momento, por meio da área "Privacidade" do Meu Perfil, tanto no aplicativo mobile do prestador quanto no portal Web do cliente, podendo confirmar que continua de acordo com os termos apresentados. |
| RF54 | Encerrar Conta ao Revogar a Concordância | Permitir que o usuário que deixar de concordar com a política encerre a conta. Após a confirmação, a conta é encerrada e os dados do usuário são removidos: fotos, clientes, tipos de serviço, agendamentos, registros financeiros, notificações e logs. |
| RF55 | Controlar a Coleta de Localização | Permitir que o usuário ative ou desative a coleta de localização no Meu Perfil. A localização só é coletada com o consentimento do usuário, para o geofencing do plano Full e enquanto o recurso estiver ativo. Ao desativar, a coleta é interrompida imediatamente. |
| RF56 | Disponibilizar Contato de Privacidade | Exibir, na política e no Meu Perfil, o e-mail de suporte para dúvidas sobre privacidade e tratamento de dados: suporte.dayplannio@gmail.com. |
| RF57 | Encerrar Conta do Prestador | Permitir que o prestador encerre sua conta pelo aplicativo mobile, por meio da área "Meu Perfil". Antes da confirmação, o sistema deve exibir um aviso informando que o encerramento da conta é permanente e que os dados associados à conta serão removidos. Após a confirmação, a conta deve ser encerrada e o prestador deve ser desconectado do aplicativo. |
| RF58 | Encerrar Conta do Cliente | Permitir que o cliente encerre sua conta pelo portal Web, por meio da área "Meu Perfil". Antes da confirmação, o sistema deve exibir um aviso informando que o encerramento da conta é permanente e que os dados associados à conta serão removidos. Após a confirmação, a conta deve ser encerrada e o cliente deve ser desconectado do portal. |
| RF59 | Encerrar Conta por Solicitação ao Administrador | Permitir que o usuário solicite o encerramento de sua conta por meio do e-mail de suporte do sistema. Após receber e verificar a solicitação, o administrador poderá realizar o encerramento da conta, removendo os dados associados conforme as regras de privacidade e proteção de dados. |

## • Requisitos não funcionais

Os requisitos não funcionais referem-se às características e restrições do sistema que não estão diretamente relacionadas às suas funcionalidades principais, mas que são essenciais para garantir sua qualidade, desempenho e usabilidade.

- **RNF1 — Desempenho:** a aplicação deve ter carregamento rápido, mesmo em conexões de internet mais lentas, para garantir uma boa experiência de usuário.
- **RNF2 — Usabilidade:** a interface da aplicação deve ser intuitiva e fácil de usar, com navegação clara e design responsivo, para que os usuários possam encontrar facilmente as informações de interesse.
- **RNF3 — Manutenibilidade:** o código-fonte da aplicação deve ser bem documentado, seguindo padrões de codificação e boas práticas de desenvolvimento, para facilitar a manutenção e futuras atualizações do sistema.
- **RNF4 — Privacidade e proteção de dados:** os dados pessoais devem ser tratados conforme a Política de Privacidade: não são vendidos nem alugados, ficam em serviços protegidos com acesso restrito, a senha não é exposta em texto puro, a localização só é coletada com o consentimento do usuário e o usuário pode solicitar a exclusão da conta e dos seus dados.

---

# 3. Modelo de casos de uso

<div align="center">

**Figura 1 – Diagrama de Caso de Uso**

<img src="imagens/diagrama-caso-uso.png" alt="Diagrama de Caso de Uso" width="80%">

*Fonte: Elaborado pelos autores (2026).*

</div>

### Casos de Uso de Alto Nível

| Caso de Uso | Descrição |
|---|---|
| Gerenciar Conta | O prestador pode se cadastrar, realizar login, recuperar a senha, editar seus dados e definir a visibilidade do telefone e da cidade. |
| Gerenciar Assinatura | O prestador pode visualizar os planos, solicitar a assinatura ou a troca de plano, aguardar a aprovação do administrador e cancelar a assinatura. |
| Gerenciar Clientes | O prestador pode cadastrar, listar e editar clientes, consultar o histórico de serviços e gerar as credenciais de acesso do cliente ao portal. |
| Gerenciar Agendamentos | O prestador pode criar, editar, cancelar, concluir e visualizar agendamentos de serviços. |
| Gerenciar Tipo de Serviço | O prestador pode cadastrar, listar, editar e excluir os tipos de serviço, incluindo tipo, descrição e tempo estimado. |
| Gerenciar Financeiro | O prestador pode registrar, editar e excluir entradas e saídas, calcular lucros e gerar relatórios financeiros. |
| Gerenciar Fotos e Portfólio | O prestador pode anexar e excluir fotos dos serviços realizados e marcá-las como públicas ou privadas para o portfólio público. |
| Monitorar Presença (Geofencing) | O prestador tem a presença no local do atendimento monitorada automaticamente por geocodificação e geofencing. |
| Consultar Métricas do Prestador | O prestador pode consultar métricas dos próprios serviços, como ganho por tipo de serviço e média de valor por serviço. |
| Acessar Portal do Cliente | O cliente pode acessar o portal web com as credenciais geradas pelo prestador, trocar a senha, definir e-mail secundário e visualizar seu perfil. |
| Consultar Métricas e Serviços Realizados | O cliente pode consultar as métricas e os serviços que já foram realizados para ele. |
| Gerenciar Usuários | O administrador pode realizar login administrativo e listar todos os prestadores e clientes cadastrados no sistema. |
| Visualizar Logs do Sistema | O administrador pode visualizar o histórico paginado de logs e ações realizadas no sistema. |
| Gerenciar Fotos | O administrador pode aprovar ou recusar as fotos enviadas pelos prestadores para o portfólio público. |
| Gerenciar Assinaturas | O administrador pode aprovar ou recusar as solicitações de assinatura e de alteração de plano dos prestadores. |
| Gerenciar Privacidade | O prestador lê e concorda com a Política de Privacidade, pode relê-la, controlar a coleta de localização e encerrar a conta com a remoção dos seus dados. |

### Casos de Uso Detalhados

<details>
<summary><b>Gerenciar Conta</b></summary>

**Ator:** Prestador (aplicativo mobile)

**Pré-condições:** o sistema está disponível; o prestador não possui cadastro (fluxo de criação) ou já possui cadastro (login/edição).

**Fluxo Principal:**
1. **Cadastro** — o prestador preenche nome completo, e-mail, senha, confirmação de senha e telefone e clica em "Cadastrar".
2. **Login** — o prestador informa e-mail e senha e é autenticado.
3. **Exibir/Editar Perfil** — o prestador visualiza seus dados, atualiza o que for necessário e clica em "Salvar".
4. **Definir Visibilidade** — o prestador define se o telefone e a cidade serão exibidos publicamente (ex.: no portfólio público) ou mantidos privados.
5. Encerrar Conta — o prestador acessa "Meu Perfil", seleciona "Encerrar Conta", visualiza o aviso sobre a exclusão dos dados e confirma o encerramento. Após a confirmação, a conta é encerrada e o prestador é desconectado do aplicativo.

**Fluxos Alternativos:**
- Campos obrigatórios não preenchidos → o sistema exibe alerta e o prestador corrige ou cancela.
- Informações em formato incorreto (ex.: e-mail sem "@", senha curta, senha e confirmação diferentes) → o sistema rejeita e exibe alerta.
- Recuperação de senha via "Esqueci minha senha" → o sistema envia link de redefinição para o e-mail cadastrado.

**Pós-condições:** conta ativa e autenticada, dados salvos e disponíveis, visibilidade do telefone e da cidade definida, acesso liberado às funcionalidades conforme o plano.
</details>

<details>
<summary><b>Gerenciar Assinatura</b></summary>

**Ator:** Prestador (aplicativo mobile). **Ator secundário:** Administrador (aprovação).

**Pré-condições:** prestador autenticado.

**Fluxo Principal:**
1. **Exibir Planos** — o prestador visualiza os planos Básico (R$ 9,90), Profissional (R$ 19,90) e Full (R$ 29,90), com as funcionalidades de cada um.
2. **Solicitar Assinatura ou Alteração** — o prestador escolhe um plano e envia a solicitação (assinatura, upgrade ou downgrade).
3. **Aguardar Aprovação** — o administrador analisa a solicitação (ver "Gerenciar Assinaturas").
4. **Ativação** — com a solicitação aprovada, o plano é ativado e as funcionalidades correspondentes são liberadas.
5. **Cancelar Assinatura** — o prestador pode cancelar o plano contratado.

**Fluxos Alternativos:**
- Solicitação recusada pelo administrador → o plano atual é mantido.
- Novo usuário → recebe 7 dias grátis no plano Full; ao término, o sistema solicita a escolha de um plano.
- Funcionalidade fora do plano contratado → o sistema bloqueia o acesso e informa o plano necessário.

**Pós-condições:** plano ativo (ou período de teste em andamento) e acesso às funcionalidades controlado conforme o plano aprovado.
</details>

<details>
<summary><b>Gerenciar Clientes</b></summary>

**Ator:** Prestador (aplicativo mobile)

**Pré-condições:** prestador autenticado.

**Fluxo Principal:**
1. **Cadastrar Cliente** — nome, telefone, endereço e observações.
2. **Gerar Credenciais** — ao cadastrar o cliente, o sistema gera automaticamente um e-mail de acesso e uma senha provisória para o portal web.
3. **Listar/Editar Clientes** — o prestador consulta e atualiza os clientes cadastrados.
4. **Consultar Histórico de Serviços** — por cliente.

**Fluxos Alternativos:** campos obrigatórios não preenchidos; informações inválidas.

**Pós-condições:** cliente cadastrado com credenciais de acesso e histórico; informações disponíveis para agendamentos e relatórios.
</details>

<details>
<summary><b>Gerenciar Agendamentos</b></summary>

**Ator:** Prestador (aplicativo mobile)

**Pré-condições:** prestador autenticado, com clientes e tipos de serviço cadastrados.

**Fluxo Principal:**
1. **Criar Agendamento** — seleciona cliente, tipo de serviço, data, hora, observações, valor cobrado e custo material, e salva.
2. **Editar Agendamento** — altera os detalhes de um serviço agendado.
3. **Cancelar Agendamento** — cancela um serviço agendado.
4. **Concluir Agendamento** — marca o serviço como concluído.
5. **Visualizar Agenda** — em modo diário, semanal ou mensal.

**Fluxos Alternativos:**
- Campos obrigatórios não preenchidos.
- Dados inválidos (horário/data).
- Conflito de agendamento no mesmo horário.

**Pós-condições:** agendamento registrado e exibido corretamente; em caso de erro, nenhuma alteração é feita.
</details>

<details>
<summary><b>Gerenciar Tipo de Serviço</b></summary>

**Ator:** Prestador (aplicativo mobile)

**Pré-condições:** prestador autenticado.

**Fluxo Principal:**
1. **Cadastrar Tipo de Serviço** — tipo, descrição e tempo estimado.
2. **Listar/Editar Tipo de Serviço**.
3. **Excluir Tipo de Serviço**.

**Fluxos Alternativos:** campos não preenchidos; valores inválidos.

**Pós-condições:** tipo de serviço cadastrado e disponível para agendamentos e relatórios.
</details>

<details>
<summary><b>Gerenciar Financeiro</b></summary>

**Ator:** Prestador (aplicativo mobile)

**Pré-condições:** prestador autenticado, com plano Profissional ou Full.

**Fluxo Principal:**
1. **Registrar Entradas e Saídas** — tipo, descrição, valor, data e categoria.
2. **Editar/Excluir Registros Financeiros**.
3. **Calcular Lucros** — lucro bruto e líquido, com base nos agendamentos concluídos e nos registros avulsos, em modo diário, semanal ou mensal.
4. **Gerar Relatórios Financeiros** — por período, exportáveis em PDF.

**Fluxos Alternativos:** dados incompletos; plano não permite o acesso ao módulo financeiro.

**Pós-condições:** entradas, saídas e lucros armazenados; relatórios exportáveis em PDF.
</details>

<details>
<summary><b>Gerenciar Fotos e Portfólio</b></summary>

**Ator:** Prestador (aplicativo mobile). **Ator secundário:** Administrador (aprovação das fotos).

**Pré-condições:** prestador autenticado, com plano Full e com agendamento realizado.

**Fluxo Principal:**
1. **Anexar Fotos** — o prestador faz o upload de fotos ao agendamento realizado.
2. **Definir Visibilidade** — cada foto é marcada como pública ou privada.
3. **Aguardar Aprovação** — as fotos públicas são analisadas pelo administrador (ver "Gerenciar Fotos").
4. **Exibição no Portfólio** — as fotos aprovadas passam a aparecer no portfólio público, visível sem necessidade de login.
5. **Excluir Foto** — o prestador pode excluir fotos cadastradas.

**Fluxos Alternativos:**
- Foto recusada pelo administrador → não é exibida no portfólio público.
- Arquivo em formato inválido → o sistema rejeita o upload.

**Pós-condições:** fotos armazenadas e portfólio público atualizado apenas com fotos aprovadas.
</details>

<details>
<summary><b>Monitorar Presença (Geofencing)</b></summary>

**Ator:** Prestador (aplicativo mobile)

**Pré-condições:** prestador autenticado, com plano Full, com agendamento criado e com permissão de localização concedida ao aplicativo.

**Fluxo Principal:**
1. **Geocodificação** — o sistema converte o endereço do agendamento em latitude e longitude.
2. **Definir Raio** — o prestador escolhe o raio de 50 m, 100 m, 200 m ou 500 m.
3. **Envio de Localização** — o aplicativo envia a localização a cada 30 segundos.
4. **Atualização de Status** — o sistema atualiza automaticamente: Agendado (atendimento criado), Em Atendimento (prestador dentro do raio), Em Pausa (prestador fora do raio por até 30 minutos) e Concluído (prestador fora do raio por 30 minutos, sem retorno ou outro atendimento autorizado).

**Fluxos Alternativos:**
- Endereço não localizado → o sistema informa e solicita a correção do endereço.
- Permissão de localização negada → o monitoramento não é iniciado.

**Pós-condições:** status do atendimento atualizado e presença do prestador registrada.
</details>

<details>
<summary><b>Consultar Métricas do Prestador</b></summary>

**Ator:** Prestador (aplicativo mobile)

**Pré-condições:** prestador autenticado, com plano Profissional ou Full.

**Fluxo Principal:**
1. **Consultar Métricas** — o prestador visualiza métricas dos próprios serviços, como ganho por tipo de serviço e média de valor por serviço.

**Fluxos Alternativos:** dados insuficientes → o sistema informa que ainda não há informações para exibir.

**Pós-condições:** métricas exibidas com base nos serviços do prestador.
</details>

<details>
<summary><b>Acessar Portal do Cliente</b></summary>

**Ator:** Cliente (plataforma web)

**Pré-condições:** cliente cadastrado pelo prestador, com e-mail de acesso e senha provisória gerados.

**Fluxo Principal:**
1. **Login** — o cliente acessa o portal com o e-mail e a senha provisória.
2. **Troca de Senha** — no primeiro acesso, o cliente é obrigado a trocar a senha provisória por uma própria.
3. **E-mail Secundário** — o cliente pode cadastrar um e-mail secundário no perfil.
4. **Exibir Perfil** — o cliente visualiza seus dados de perfil.
5. Encerrar Conta — o cliente acessa "Meu Perfil", seleciona "Encerrar Conta", visualiza o aviso sobre a exclusão dos dados e confirma o encerramento. Após a confirmação, a conta é encerrada e o cliente é desconectado do portal.

**Fluxos Alternativos:**
- Credenciais inválidas → o sistema rejeita o acesso e exibe alerta.
- Recuperação de senha → o cliente solicita e realiza a redefinição pelo portal.
- Nova senha e confirmação diferentes → o sistema rejeita e exibe alerta.

**Pós-condições:** cliente autenticado com senha própria e acesso liberado ao portal.
</details>

<details>
<summary><b>Consultar Métricas e Serviços Realizados</b></summary>

**Ator:** Cliente (plataforma web)

**Pré-condições:** cliente autenticado no portal, com prestador no plano Full.

**Fluxo Principal:**
1. **Consultar Serviços Realizados** — o cliente visualiza os serviços que já foram realizados para ele.
2. **Consultar Métricas** — o cliente visualiza métricas desses serviços, como os últimos serviços e a média de tempo por serviço.

**Fluxos Alternativos:** nenhum serviço realizado até o momento → o sistema informa que não há informações para exibir.

**Pós-condições:** métricas e serviços exibidos apenas com os dados do próprio cliente.
</details>

<details>
<summary><b>Gerenciar Usuários</b></summary>

<b>Ator:</b> Administrador (plataforma web)

<b>Pré-condições:</b> administrador cadastrado no sistema.

<b>Fluxo Principal:</b>

<b>Login Administrativo</b> — o administrador acessa o portal web, separado do acesso dos prestadores.
<b>Listar Prestadores</b> — visualiza todos os prestadores cadastrados.
<b>Listar Clientes</b> — visualiza todos os clientes cadastrados, de todos os prestadores.
<b>Encerrar Conta por Solicitação</b> — o administrador recebe uma solicitação de encerramento de conta enviada pelo usuário por meio do e-mail de suporte e, após verificar a solicitação, encerra a conta correspondente.

<b>Fluxos Alternativos:</b> credenciais inválidas → o sistema rejeita o acesso e exibe alerta.

<b>Pós-condições:</b> administrador autenticado com acesso às listas de usuários e possibilidade de encerrar contas mediante solicitação.
</details>

<details>
<summary><b>Visualizar Logs do Sistema</b></summary>

**Ator:** Administrador (plataforma web)

**Pré-condições:** administrador autenticado.

**Fluxo Principal:**
1. **Consultar Logs** — o administrador visualiza o histórico paginado de logs e ações realizadas no sistema.

**Fluxos Alternativos:** nenhum registro disponível → o sistema informa que o histórico está vazio.

**Pós-condições:** logs exibidos sem alteração dos registros.
</details>

<details>
<summary><b>Gerenciar Fotos</b></summary>

**Ator:** Administrador (plataforma web)

**Pré-condições:** administrador autenticado e fotos públicas enviadas por prestadores aguardando análise.

**Fluxo Principal:**
1. **Analisar Fotos** — o administrador visualiza as fotos de atendimento enviadas pelos prestadores.
2. **Aprovar ou Recusar** — o administrador aprova ou recusa cada foto.
3. **Publicação** — as fotos aprovadas passam a ser exibidas no portfólio público.

**Fluxos Alternativos:** foto recusada → não é exibida no portfólio público.

**Pós-condições:** portfólio público contém apenas fotos aprovadas.
</details>

<details>
<summary><b>Gerenciar Assinaturas</b></summary>

**Ator:** Administrador (plataforma web)

**Pré-condições:** administrador autenticado e solicitações de assinatura ou de alteração de plano enviadas por prestadores.

**Fluxo Principal:**
1. **Analisar Solicitações** — o administrador visualiza as solicitações pendentes.
2. **Aprovar ou Recusar** — o administrador aprova ou recusa cada solicitação.
3. **Ativação do Plano** — com a aprovação, o plano do prestador é ativado ou alterado.

**Fluxos Alternativos:** solicitação recusada → o plano atual do prestador é mantido.

**Pós-condições:** plano do prestador atualizado conforme a decisão do administrador.
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
- **Diferenciais:** foco total nas necessidades de quem trabalha por conta própria, sistema de fácil aprendizado, comprovação de presença no local do atendimento por geofencing, portal web para o cliente acompanhar os serviços realizados para ele, portfólio público para divulgação do trabalho e planos de assinatura de baixo custo, com 7 dias grátis para novos usuários.
- **Clientes Potenciais:** trabalhadores autônomos da região e os clientes atendidos por esses profissionais.

### Viabilidade Técnica

- **Recursos Humanos:** execução conduzida pelos próprios alunos, autores do trabalho.
- **Ferramentas:** C# (linguagem), ASP.NET (backend/API), .NET MAUI (aplicativo mobile multiplataforma do prestador), ASP.NET (plataforma web cliente e administrador), MongoDB (banco de dados), Git e GitHub (versionamento).
- **Hospedagem em nuvem:** o banco de dados será hospedado no MongoDB Atlas, e o projeto (API e plataforma web) e o armazenamento das fotos de serviço ficarão no Microsoft Azure.
- **Serviços de apoio:** geocodificação e mapas (monitoramento de presença) e envio de e-mails (credenciais e recuperação de senha).
- **Infraestrutura tecnológica:** computadores e conexão à internet disponibilizados pela FATEC-JAHU para o desenvolvimento, e serviços em nuvem para a execução do sistema.

### Viabilidade Operacional

- **Fluxo de Trabalho Simplificado:** foco apenas em informações essenciais para o gerenciamento pelo prestador.
- **Acessibilidade e Usabilidade:** interface intuitiva, reduzindo problemas de entendimento do sistema, com o aplicativo mobile para o prestador e o portal web para o cliente e o administrador.
- **Disponibilidade:** a hospedagem em nuvem permite acessar o aplicativo e o portal web a qualquer momento e de qualquer lugar, sem que o usuário precise manter servidores próprios.
- **Geração de Lucros e valores imediatos:** o sistema registra automaticamente os valores inseridos no cálculo do lucro final.
- **Controle de Acesso e Moderação:** as funcionalidades são liberadas conforme o plano contratado, e o administrador aprova as fotos do portfólio público e as solicitações de assinatura.

### Viabilidade Econômica

- **Investimento inicial:** desenvolvimento, teste, validação e publicação do aplicativo e da plataforma web, custos com ferramentas pagas.
- **Custos recorrentes:** hospedagem em nuvem (MongoDB Atlas para o banco de dados e Microsoft Azure para o projeto e o armazenamento de fotos), envio de e-mails, geocodificação, suporte, atualização, manutenção e divulgação do produto.
- **Fontes de receita:** assinaturas mensais em três planos (Básico, Profissional e Full), com 7 dias grátis no plano Full para novos usuários.
- **Benefícios Financeiros:** melhor controle financeiro, visualização clara de lucros e despesas, maior organização e produtividade.

### Conclusão do Estudo de Viabilidade

Após a análise dos aspectos de mercado, técnicos, operacionais e econômicos, conclui-se que o projeto é viável e coerente com seus objetivos. As tecnologias escolhidas são compatíveis com os recursos disponíveis, a aplicação é de fácil operação, e a proposta atende a uma necessidade real de organização da rotina de profissionais autônomos. Além disso, o modelo de assinaturas em planos oferece uma fonte de receita para a manutenção do produto. Portanto, o projeto demonstra potencial para ser implementado e aprimorado futuramente.

---

# 8. Regras de negócio (Modelo canvas)

Para a elaboração do modelo de negócio, foi utilizado o **Modelo de Negócio Canvas**, permitindo planejar de forma concisa e visual os principais aspectos da aplicação web, como público-alvo, proposta de valor, canais de distribuição, fontes de receita e estrutura de custos.

<div align="center">

**Figura 2 – Modelo de Negócio Canvas**

<img src="imagens/modelo-negocio-canvas.png" alt="Modelo de Negócio Canvas" width="80%">

*Fonte: Elaborado pelos autores (2026).*

</div>

### O que será elaborado?

**Proposta de valor:** um aplicativo mobile com interface intuitiva, que permite ao prestador de serviços utilizá-lo sem necessitar de muito aprendizado sobre a plataforma. O DayPlannio substitui o trabalho manual por um gerenciamento automático e simplificado de agenda, clientes, serviços e finanças. Também oferece:

- Comprovação de presença no local do atendimento por geolocalização e geofencing;
- Portal web para o cliente acompanhar suas métricas e os serviços prestados a ele;
- Portfólio público para divulgar o trabalho do profissional.

### Como será elaborado?

**Parcerias principais:**

- FATEC Jahu: fornece a infraestrutura física e a orientação técnica;
- Trabalhadores autônomos: responsáveis pela validação do aplicativo;
- Empresa colaboradora: Gabriel Serviços Gerais;
- Provedores de mapas e geocodificação: viabilizam o monitoramento de presença por geofencing;
- Serviço de e-mail: envio de credenciais e recuperação de senha.

**Atividades principais:**

- Prestador (mobile): gerenciar agendamentos e serviços; gerenciar clientes e histórico; registrar entradas e saídas, calcular lucros e gerar relatórios financeiros; gerar credenciais e acesso do cliente; monitorar presença por geofencing;
- Administrador (web): moderar fotos e manter o portfólio público; administrar usuários, acessos e logs do sistema;
- Cliente (web): consultar métricas e serviços prestados a ele.

**Recursos principais:**

- Aplicativo mobile (prestador) e plataforma web (cliente e administrador);
- Equipe de desenvolvimento;
- Dados de clientes, serviços, agenda e financeiro;
- Armazenamento de fotos de serviço;
- Serviços de geolocalização.

### Para quem será elaborado?

**Relacionamento com clientes:**

- Suporte ao usuário;
- Aprendizado prático no uso da plataforma;
- 7 dias grátis para novos usuários.

**Canais:**

- Aplicativo mobile (prestador);
- Plataforma web (cliente e administrador);
- Portfólio público;
- Parcerias locais e recomendações pessoais.

**Segmento de clientes:**

- Profissionais autônomos que precisam organizar agenda, clientes, serviços e registros financeiros;
- Profissionais que desejam acompanhar pagamentos, lucros e histórico de atendimentos;
- Clientes dos profissionais, que acompanham métricas e os serviços prestados a eles pelo portal web;
- Administradores da plataforma web, responsáveis por usuários, logs e aprovação de fotos.

### Quanto vai custar?

**Estrutura de custos:**

- Desenvolvimento e manutenção do aplicativo mobile e da plataforma web;
- Infraestrutura e serviços necessários ao sistema (hospedagem, armazenamento de fotos, e-mail e geocodificação);
- Suporte e atualização;
- Divulgação.

**Fontes de receita:** assinaturas mensais, divididas em três planos:

| Plano | Valor | Funcionalidades |
|---|---|---|
| Básico | R$&nbsp;9,90 | Criar, editar e cancelar agendamentos; visualizar agenda; cadastrar clientes; histórico de clientes; cadastrar tipos de serviço; perfil do profissional |
| Profissional | R$&nbsp;19,90 | Tudo do Básico; entradas e saídas financeiras; cálculo de lucro e lucro geral; relatórios financeiros; métricas do prestador |
| Full | R$&nbsp;29,90 | Tudo do Profissional; portfólio público; upload de fotos dos serviços; área do cliente e métricas do cliente; geolocalização e geofencing |

Novos usuários ganham 7 dias grátis no plano Full, para testar todos os recursos da plataforma antes de escolher o plano ideal.

---

# 9. Design

O design do DayPlannio é centrado na experiência do usuário, com uma interface limpa, intuitiva e organizada que facilita o gerenciamento da rotina de profissionais autônomos.

### Paleta de cores

<div align="center">

**Figura 3 – Paleta de Cores**

<img src="imagens/paleta-cores.png" alt="Paleta de Cores" width="80%">

*Fonte: Elaborado pelos autores (2026).*

</div>

A paleta de cores do DayPlannio foi cuidadosamente selecionada para transmitir organização, produtividade, simplicidade e confiança, refletindo o propósito da aplicação de auxiliar profissionais autônomos na gestão de sua rotina de forma prática e eficiente.

### Tipografia

A tipografia é um aspecto fundamental do design do DayPlannio, pois influencia diretamente a legibilidade, a estética e a experiência do usuário. Para o desenvolvimento da interface do aplicativo mobile, foi escolhida a fonte Open Sans, reconhecida por sua clareza, modernidade e versatilidade, características importantes para a leitura em telas pequenas. A Figura 4 apresenta um exemplo de utilização da fonte no aplicativo. Já no portal web, utiliza-se a fonte Segoe UI, com a fonte padrão do sistema como alternativa, o que garante boa leitura e carregamento rápido nos navegadores. A Figura 5 apresenta um exemplo de utilização dessa fonte no portal.

<div align="center">

**Figura 4 – Exemplo Fonte Open Sans**

<img src="imagens/fonte-open-sans.png" alt="Exemplo Fonte Open Sans" width="80%">

*Fonte: Adobe (2026).*

</div>

<div align="center">

**Figura 5 – Exemplo Fonte Segoe UI**

<img src="imagens/fonte.png" alt="Exemplo Fonte Segoe UI" width="80%">

*Fonte: Adobe (2026).*

</div>

### Isotipo

O isotipo escolhido para o DayPlannio desempenha um papel importante na representação visual da aplicação e na comunicação de sua identidade voltada à organização, produtividade e gestão de atividades, buscando transmitir a ideia de planejamento, controle da rotina e praticidade no dia a dia dos profissionais autônomos.

<div align="center">

**Figura 6 – Isotipo**

<img src="imagens/isotipo.png" alt="Isotipo DayPlannio" width="60%">

*Fonte: Elaborado pelos autores (2026).*

</div>

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

<h3 align="center">Cadastro e acesso</h3>
<table>
<tr>
<td align="center">

<img src="imagens/cadastro-usuario.png" alt="Cadastro de Usuário" width="45%">

<strong>Cadastro de Usuário</strong>
</td>
<td align="center">

<img src="imagens/login-usuario.png" alt="Login de Usuário" width="45%">

<strong>Login de Usuário</strong>
</td>
</tr>
</table>

<table>
<tr>
<td align="center">

<img src="imagens/redefinicao-senha.png" alt="Redefinição de Senha" width="45%">

<strong>Redefinição de Senha</strong>
</td>
<td align="center">

<img src="imagens/confirmar-codigo.png" alt="Confirmar Código" width="45%">

<strong>Confirmar Código</strong>
</td>
</tr>
</table>

<table>
<tr>
<td align="center">

<img src="imagens/nova-senha.png" alt="Nova Senha" width="45%">

<strong>Nova Senha</strong>
</td>
</tr>
</table>

<h3 align="center">Agendamentos</h3>
<table>
<tr>
<td align="center">

<img src="imagens/agendamentos.png" alt="Agendamentos" width="45%">

<strong>Agendamentos</strong>
</td>
<td align="center">

<img src="imagens/cadastrar-agendamento.png" alt="Cadastrar Agendamento" width="45%">

<strong>Cadastrar Agendamento</strong>
</td>
</tr>
</table>

<table>
<tr>
<td align="center">

<img src="imagens/editar-agendamento.png" alt="Editar Agendamento" width="45%">

<strong>Editar Agendamento</strong>
</td>
<td align="center">

<img src="imagens/concluir-agendamento.png" alt="Concluir Agendamento" width="45%">

<strong>Concluir Agendamento</strong>
</td>
</tr>
</table>

<table>
<tr>
<td align="center">

<img src="imagens/cancelar-agendamento.png" alt="Cancelar Agendamento" width="45%">

<strong>Cancelar Agendamento</strong>
</td>
<td align="center">

<img src="imagens/excluir-agendamento.png" alt="Excluir Agendamento" width="45%">

<strong>Excluir Agendamento</strong>
</td>
</tr>
</table>

<h3 align="center">Clientes</h3>
<table>
<tr>
<td align="center">

<img src="imagens/clientes.png" alt="Clientes" width="45%">

<strong>Clientes</strong>
</td>
<td align="center">

<img src="imagens/cadastrar-cliente.png" alt="Cadastrar Cliente" width="45%">

<strong>Cadastrar Cliente</strong>
</td>
</tr>
</table>

<table>
<tr>
<td align="center">

<img src="imagens/editar-cliente.png" alt="Editar Cliente" width="45%">

<strong>Editar Cliente</strong>
</td>
<td align="center">

<img src="imagens/excluir-cliente.png" alt="Excluir Cliente" width="45%">

<strong>Excluir Cliente</strong>
</td>
</tr>
</table>

<table>
<tr>
<td align="center">

<img src="imagens/historico-cliente.png" alt="Histórico do Cliente" width="45%">

<strong>Histórico do Cliente</strong>
</td>
</tr>
</table>

<h3 align="center">Serviços</h3>
<table>
<tr>
<td align="center">

<img src="imagens/servicos.png" alt="Serviços" width="45%">

<strong>Serviços</strong>
</td>
<td align="center">

<img src="imagens/cadastrar-servico.png" alt="Cadastrar Serviço" width="45%">

<strong>Cadastrar Serviço</strong>
</td>
</tr>
</table>

<table>
<tr>
<td align="center">

<img src="imagens/editar-servico.png" alt="Editar Serviço" width="45%">

<strong>Editar Serviço</strong>
</td>
<td align="center">

<img src="imagens/excluir-servico.png" alt="Excluir Serviço" width="45%">

<strong>Excluir Serviço</strong>
</td>
</tr>
</table>

<h3 align="center">Entradas e Saídas</h3>
<table>
<tr>
<td align="center">

<img src="imagens/cadastro-entrada-saida.png" alt="Cadastro de Entrada e Saída" width="45%">

<strong>Cadastro de Entrada e Saída</strong>
</td>
<td align="center">

<img src="imagens/editar-entrada-saida.png" alt="Editar Entrada e Saída" width="45%">

<strong>Editar Entrada e Saída</strong>
</td>
</tr>
</table>

<table>
<tr>
<td align="center">

<img src="imagens/excluir-entrada-saida.png" alt="Excluir Entrada e Saída" width="45%">

<strong>Excluir Entrada e Saída</strong>
</td>
</tr>
</table>

<h3 align="center">Movimentações</h3>
<table>
<tr>
<td align="center">

<img src="imagens/movimentacoes-diarias.png" alt="Movimentações Diárias" width="45%">

<strong>Movimentações Diárias</strong>
</td>
<td align="center">

<img src="imagens/movimentacoes-semanais.png" alt="Movimentações Semanais" width="45%">

<strong>Movimentações Semanais</strong>
</td>
</tr>
</table>

<table>
<tr>
<td align="center">

<img src="imagens/movimentacoes-mensais.png" alt="Movimentações Mensais" width="45%">

<strong>Movimentações Mensais</strong>
</td>
</tr>
</table>

<h3 align="center">Resumos</h3>
<table>
<tr>
<td align="center">

<img src="imagens/resumos-diarios.png" alt="Resumos Diários" width="45%">

<strong>Resumos Diários</strong>
</td>
<td align="center">

<img src="imagens/resumos-semanais.png" alt="Resumos Semanais" width="45%">

<strong>Resumos Semanais</strong>
</td>
</tr>
</table>

<table>
<tr>
<td align="center">

<img src="imagens/resumos-mensais.png" alt="Resumos Mensais" width="45%">

<strong>Resumos Mensais</strong>
</td>
</tr>
</table>

<h3 align="center">Perfil</h3>
<table>
<tr>
<td align="center">

<img src="imagens/editar-perfil.png" alt="Editar Perfil" width="45%">

<strong>Editar Perfil</strong>
</td>
</tr>
</table>

---

# 12. Considerações finais

O desenvolvimento deste projeto contribuiu para o aprimoramento das habilidades da equipe em planejamento, trabalho em equipe e resolução de problemas durante o processo de desenvolvimento. Além disso, a aplicação oferece suporte aos trabalhadores autônomos, auxiliando na organização de suas atividades e no controle financeiro, tornando a rotina de trabalho mais prática, eficiente e organizada.

---

# 13. Referências

- ADOBE. **Open Sans.** Disponível em: <https://fonts.adobe.com/fonts/open-sans>. Acesso em: 15 abr. 2026.
- ADOBE. **Segoe UI.** Disponível em: <https://fonts.adobe.com/fonts/segoe-ui>. Acesso em: 6 out. 2026.
- CANVA. **Canva**. Disponível em: <https://www.canva.com/pt_br/>. Acesso em: mar. 2026.
- FIGMA. **Figma**. Disponível em: <https://www.figma.com>. Acesso em: abr. 2026.
- LUCIDCHART. **LucidChart**. Disponível em: <https://www.lucidchart.com>. Acesso em: abr. 2026.
- MICROSOFT. **Visual Studio**. Disponível em: <https://visualstudio.microsoft.com>. Acesso em: abr. 2026.
- MONGODB, Inc. **MongoDB**. Disponível em: <https://www.mongodb.com>. Acesso em: abr. 2026.
- GITHUB. **GitHub**. Disponível em: <https://github.com>. Acesso em: abr. 2026.
- TRELLO. **Trello**. Disponível em: <https://trello.com/pt-BR>. Acesso em: abr. 2026.
