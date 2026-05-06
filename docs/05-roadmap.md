# 05 — Roadmap

## 🚀 AcademyFLOW — Plano de Evolução do Projeto

O roadmap do **AcademyFLOW** apresenta as fases previstas para o desenvolvimento do sistema, desde a documentação inicial até a implementação futura de funcionalidades inteligentes, lembretes, integração com calendário e interação por voz.

A proposta é evoluir o projeto de forma gradual, organizada e acessível, priorizando primeiro a estrutura conceitual e depois a construção técnica.

---

## 🎯 Objetivo do Roadmap

O roadmap tem como objetivo:

- Organizar as etapas de desenvolvimento do AcademyFLOW
- Definir entregas por fase
- Evitar que o projeto fique confuso ou grande demais no início
- Facilitar a construção incremental do sistema
- Apoiar a documentação do projeto para portfólio
- Permitir evolução futura com IA, voz e calendário

---

## 🧭 Visão Geral das Fases

| Fase | Nome | Objetivo |
|---|---|---|
| 1 | Documentação Inicial | Estruturar a ideia, problema, solução e escopo |
| 2 | Base de Dados | Definir os arquivos e campos do sistema |
| 3 | Protótipo Visual | Criar a primeira interface do AcademyFLOW |
| 4 | Cadastro Acadêmico | Implementar cadastro de disciplinas, atividades e observações |
| 5 | Lembretes e Prioridades | Organizar prazos, lembretes e tarefas urgentes |
| 6 | Agente Flowup | Criar o assistente acadêmico inteligente |
| 7 | Integração com Calendário | Avaliar integração com Google Calendar ou Outlook |
| 8 | Entrada por Voz | Permitir que o usuário registre informações falando |
| 9 | Resposta por Voz | Permitir que o agente responda por áudio |
| 10 | Evolução para App | Avaliar versão web/mobile mais completa |

---

## ✅ Fase 1 — Documentação Inicial

### Objetivo

Criar a base conceitual do projeto AcademyFLOW.

### Entregas

- README principal
- Documentação do sistema
- Base de conhecimento
- Prompts do agente Flowup
- Métricas de avaliação
- Roadmap do projeto

### Status

```text
Em andamento
```

---

## ✅ Fase 2 — Base de Dados

### Objetivo

Definir a estrutura inicial dos dados usados pelo sistema.

### Entregas previstas

- Criar pasta `data/`
- Criar arquivo `disciplinas.json`
- Criar arquivo `atividades.json`
- Criar arquivo `calendario_academico.json`
- Criar arquivo `lembretes.json`
- Criar arquivo `observacoes.json`
- Inserir dados fictícios para teste

### Critério de conclusão

A fase será considerada concluída quando os arquivos JSON estiverem criados e puderem ser carregados pela aplicação.

---

## ✅ Fase 3 — Protótipo Visual

### Objetivo

Criar a primeira versão da interface do AcademyFLOW.

### Tecnologias possíveis

- Python
- Streamlit

### Entregas previstas

- Tela inicial do sistema
- Menu lateral
- Área para cadastro de disciplinas
- Área para cadastro de atividades
- Área para observações
- Área para consulta ao Flowup

### Critério de conclusão

A fase será considerada concluída quando o usuário conseguir navegar pela interface e visualizar as seções principais.

---

## ✅ Fase 4 — Cadastro Acadêmico

### Objetivo

Permitir que o estudante registre suas informações acadêmicas.

### Funcionalidades previstas

- Cadastro de disciplinas
- Cadastro de provas
- Cadastro de trabalhos
- Cadastro de seminários
- Cadastro de segunda chamada
- Cadastro de recuperação
- Cadastro de DP
- Cadastro de observações livres
- Edição de registros
- Exclusão de registros

### Critério de conclusão

A fase será considerada concluída quando o usuário conseguir cadastrar, visualizar, editar e excluir informações acadêmicas básicas.

---

## ✅ Fase 5 — Lembretes e Prioridades

### Objetivo

Organizar as atividades por prazo, urgência e importância.

### Funcionalidades previstas

- Criar lembretes opcionais
- Listar tarefas pendentes
- Identificar tarefas atrasadas
- Destacar atividades críticas
- Organizar prioridades por data
- Exibir resumo do dia
- Exibir resumo da semana

### Critério de conclusão

A fase será considerada concluída quando o sistema conseguir listar atividades por ordem de prioridade e destacar prazos importantes.

---

## ✅ Fase 6 — Agente Flowup

### Objetivo

Implementar o agente inteligente do AcademyFLOW.

### Funcionalidades previstas

- Consultar dados cadastrados
- Responder perguntas sobre prazos
- Listar prioridades
- Identificar tarefas atrasadas
- Explicar limitações quando faltar informação
- Evitar respostas inventadas
- Manter foco no escopo acadêmico

### Exemplos de perguntas suportadas

```text
O que eu tenho para fazer hoje?
Tenho prova essa semana?
Qual tarefa devo priorizar?
O que está atrasado?
Tenho alguma DP pendente?
Quais matérias preciso estudar?
```

### Critério de conclusão

A fase será considerada concluída quando o Flowup conseguir responder perguntas simples com base nos dados cadastrados.

---

## ✅ Fase 7 — Integração com Calendário

### Objetivo

Avaliar formas de sincronizar prazos e lembretes com calendários externos.

### Possibilidades futuras

- Google Calendar
- Outlook Calendar
- Exportação de eventos em arquivo `.ics`
- Geração manual de lembretes para copiar no calendário

### Observação

A integração com calendários pode depender de autenticação, permissões e APIs externas. Por isso, inicialmente, o projeto poderá priorizar alternativas gratuitas e simples.

### Critério de conclusão

A fase será considerada concluída quando o sistema conseguir gerar ou sincronizar eventos acadêmicos com algum tipo de calendário.

---

## ✅ Fase 8 — Entrada por Voz

### Objetivo

Permitir que o estudante registre informações acadêmicas por voz.

### Exemplo de uso

```text
Flowup, anota que tenho prova de Banco de Dados na próxima sexta-feira.
```

### Possibilidades técnicas

- Reconhecimento de voz local
- Whisper em ambiente gratuito/local
- Entrada de áudio no navegador
- Transcrição para texto

### Critério de conclusão

A fase será considerada concluída quando o usuário conseguir falar uma informação e o sistema converter em texto para registro ou análise.

---

## ✅ Fase 9 — Resposta por Voz

### Objetivo

Permitir que o Flowup responda ao estudante por áudio.

### Exemplo de resposta

```text
Você tem uma entrega importante na sexta-feira. Minha sugestão é priorizar essa atividade hoje.
```

### Possibilidades técnicas

- gTTS
- pyttsx3
- Recursos nativos do navegador
- Síntese de voz local ou gratuita

### Critério de conclusão

A fase será considerada concluída quando o sistema conseguir transformar a resposta textual do Flowup em áudio.

---

## ✅ Fase 10 — Evolução para App

### Objetivo

Avaliar uma versão mais completa do AcademyFLOW como aplicação web ou mobile.

### Possibilidades futuras

- Aplicação web responsiva
- Aplicativo mobile
- Login de usuário
- Banco de dados em nuvem
- Notificações reais
- Dashboard acadêmico
- Histórico de atividades
- Relatórios de produtividade acadêmica

### Critério de conclusão

A fase será considerada concluída quando houver definição clara sobre a melhor plataforma para evolução do projeto.

---

## 🧩 Backlog de Funcionalidades Futuras

| Funcionalidade | Prioridade | Observação |
|---|---|---|
| Cadastro de disciplinas | Alta | Base do sistema |
| Cadastro de atividades | Alta | Essencial para o Flowup |
| Campo de observações | Alta | Importante para registros livres |
| Lembretes opcionais | Alta | Ajuda na rotina acadêmica |
| Priorização automática | Alta | Diferencial do sistema |
| Agente Flowup | Alta | Núcleo inteligente do projeto |
| Integração com calendário | Média | Depende de permissões/APIs |
| Entrada por voz | Média | Pode ser feita em etapa futura |
| Resposta por voz | Média | Complementa a acessibilidade |
| Dashboard de desempenho | Baixa | Evolução futura |
| Versão mobile | Baixa | Após validação do protótipo |

---

## 📌 MVP — Produto Mínimo Viável

A primeira versão funcional do AcademyFLOW deverá conter apenas o essencial para validar a ideia.

### MVP previsto

- Cadastro de disciplinas
- Cadastro de atividades
- Cadastro de observações
- Listagem de tarefas pendentes
- Identificação de tarefas próximas do prazo
- Consulta simples ao Flowup
- Respostas baseadas apenas nos dados cadastrados

### Fora do MVP inicial

- Login de usuário
- Banco de dados em nuvem
- Integração real com calendário
- Notificações automáticas externas
- Entrada e resposta por voz
- Aplicativo mobile

---

## 🧠 Estratégia de Desenvolvimento

O projeto deverá ser desenvolvido por partes, evitando tentar implementar tudo de uma vez.

A ordem recomendada é:

1. Finalizar documentação
2. Criar arquivos de dados
3. Criar interface simples
4. Implementar cadastro
5. Implementar listagem
6. Implementar prioridades
7. Implementar Flowup básico
8. Validar com testes
9. Melhorar interface
10. Planejar integrações futuras

---

## ✅ Resultado Esperado

Com esse roadmap, o AcademyFLOW poderá evoluir de forma organizada, mantendo foco no problema real: ajudar estudantes a organizar melhor suas disciplinas, atividades, prazos e prioridades.

A documentação funciona como guia para o desenvolvimento técnico e também como material de portfólio, demonstrando planejamento, visão de produto, engenharia de software e aplicação responsável de inteligência artificial.
