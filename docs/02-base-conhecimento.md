# 02 — Base de Conhecimento

## 🎓 AcademyFLOW — Base Acadêmica do Sistema

A **Base de Conhecimento** do AcademyFLOW representa o conjunto de dados acadêmicos que serão cadastrados pelo estudante e utilizados pelo agente **Flowup** para organizar informações, gerar lembretes, identificar prioridades e responder perguntas sobre a rotina de estudos.

O objetivo dessa base é centralizar informações que normalmente ficam espalhadas em diferentes lugares, como caderno, agenda, e-mail, grupos de mensagens, plataformas acadêmicas e calendários.

---

## 🎯 Objetivo da Base de Conhecimento

A base de conhecimento tem como objetivo:

- Organizar disciplinas cadastradas pelo estudante
- Registrar provas, trabalhos, seminários e atividades
- Armazenar prazos importantes
- Controlar lembretes acadêmicos
- Registrar observações livres
- Apoiar o agente Flowup na análise de prioridades
- Evitar que o sistema invente informações não cadastradas

---

## 🗂️ Dados Utilizados

| Arquivo | Tipo | Finalidade |
|---|---|---|
| `disciplinas.json` | JSON | Armazena as disciplinas/matérias cadastradas pelo estudante |
| `atividades.json` | JSON | Armazena provas, trabalhos, seminários, segunda chamada, recuperação, DP e demais tarefas |
| `calendario_academico.json` | JSON | Guarda datas importantes do semestre ou período letivo |
| `lembretes.json` | JSON | Registra lembretes configurados pelo usuário |
| `observacoes.json` | JSON | Armazena anotações livres, recados e informações complementares |

---

## 📘 `disciplinas.json`

Esse arquivo deverá guardar as informações principais sobre cada disciplina cadastrada.

### Exemplo de estrutura

```json
[
  {
    "id": 1,
    "nome": "Engenharia de Software",
    "professor": "Nome do Professor",
    "curso": "Engenharia de Software",
    "semestre": "6º semestre",
    "dias_aula": ["terça-feira", "quinta-feira"],
    "status": "em andamento",
    "observacoes": "Disciplina com foco em requisitos, modelagem e documentação."
  }
]
```

### Campos previstos

| Campo | Descrição |
|---|---|
| `id` | Identificador único da disciplina |
| `nome` | Nome da disciplina |
| `professor` | Nome do professor, se informado |
| `curso` | Curso relacionado |
| `semestre` | Semestre ou período |
| `dias_aula` | Dias em que a disciplina acontece |
| `status` | Status da disciplina: em andamento, concluída, pendente ou DP |
| `observacoes` | Campo livre para informações adicionais |

---

## 📝 `atividades.json`

Esse arquivo será usado para registrar todas as demandas acadêmicas do estudante.

### Tipos de atividades previstos

- Prova
- Trabalho
- Seminário
- Atividade complementar
- Leitura obrigatória
- Segunda chamada
- Recuperação
- DP
- Revisão de conteúdo
- Entrega de projeto
- Outro

### Exemplo de estrutura

```json
[
  {
    "id": 1,
    "disciplina_id": 1,
    "titulo": "Entrega da documentação do projeto",
    "tipo": "trabalho",
    "descricao": "Finalizar README, documentação técnica e organização dos arquivos.",
    "data_entrega": "2026-05-15",
    "prioridade": "alta",
    "status": "pendente",
    "lembrete": true,
    "data_lembrete": "2026-05-13"
  }
]
```

### Campos previstos

| Campo | Descrição |
|---|---|
| `id` | Identificador único da atividade |
| `disciplina_id` | Relaciona a atividade com uma disciplina cadastrada |
| `titulo` | Nome curto da atividade |
| `tipo` | Tipo da atividade: prova, trabalho, seminário, segunda chamada, recuperação, DP etc. |
| `descricao` | Detalhes da atividade |
| `data_entrega` | Data de entrega, prova ou realização |
| `prioridade` | Baixa, média, alta ou crítica |
| `status` | Pendente, em andamento, concluída, atrasada ou cancelada |
| `lembrete` | Indica se o estudante deseja receber lembrete |
| `data_lembrete` | Data planejada para lembrete |

---

## 📅 `calendario_academico.json`

Esse arquivo será usado para registrar datas importantes do período acadêmico.

### Exemplo de estrutura

```json
[
  {
    "id": 1,
    "titulo": "Início do semestre",
    "data": "2026-02-10",
    "tipo": "calendario academico",
    "descricao": "Data oficial de início das aulas."
  },
  {
    "id": 2,
    "titulo": "Período de provas finais",
    "data_inicio": "2026-06-10",
    "data_fim": "2026-06-20",
    "tipo": "provas finais",
    "descricao": "Período reservado para avaliações finais."
  }
]
```

### Campos previstos

| Campo | Descrição |
|---|---|
| `id` | Identificador único do evento |
| `titulo` | Nome do evento acadêmico |
| `data` | Data única do evento, quando aplicável |
| `data_inicio` | Data inicial, quando for um período |
| `data_fim` | Data final, quando for um período |
| `tipo` | Tipo do evento: início de semestre, prova, recesso, prazo institucional etc. |
| `descricao` | Informações complementares |

---

## ⏰ `lembretes.json`

Esse arquivo armazenará os lembretes criados pelo usuário.

### Exemplo de estrutura

```json
[
  {
    "id": 1,
    "atividade_id": 1,
    "titulo": "Revisar documentação do projeto",
    "data_lembrete": "2026-05-13",
    "horario": "19:00",
    "canal": "app",
    "status": "ativo"
  }
]
```

### Campos previstos

| Campo | Descrição |
|---|---|
| `id` | Identificador único do lembrete |
| `atividade_id` | Atividade vinculada ao lembrete, se houver |
| `titulo` | Título do lembrete |
| `data_lembrete` | Data em que o lembrete deverá aparecer |
| `horario` | Horário previsto |
| `canal` | Local do lembrete: app, calendário, e-mail ou outro canal futuro |
| `status` | Ativo, concluído ou cancelado |

---

## 🗒️ `observacoes.json`

Esse arquivo será usado para guardar observações livres, permitindo que o estudante registre qualquer informação importante.

### Exemplo de estrutura

```json
[
  {
    "id": 1,
    "disciplina_id": 1,
    "titulo": "Orientação do professor",
    "conteudo": "O professor informou que a entrega poderá ser feita até sexta-feira.",
    "data_registro": "2026-05-06",
    "criar_lembrete": true,
    "data_lembrete": "2026-05-09"
  }
]
```

### Campos previstos

| Campo | Descrição |
|---|---|
| `id` | Identificador único da observação |
| `disciplina_id` | Disciplina vinculada, se houver |
| `titulo` | Título curto da observação |
| `conteudo` | Texto livre registrado pelo estudante |
| `data_registro` | Data em que a observação foi criada |
| `criar_lembrete` | Indica se a observação deve gerar lembrete |
| `data_lembrete` | Data planejada para o lembrete, se aplicável |

---

## 🤖 Como o Flowup Usa a Base de Conhecimento

O agente **Flowup** deverá consultar a base de conhecimento para responder perguntas do estudante de forma contextualizada.

### Exemplos de perguntas

| Pergunta do estudante | Dados consultados |
|---|---|
| O que tenho para fazer hoje? | `atividades.json`, `lembretes.json` |
| Tenho prova essa semana? | `atividades.json`, `calendario_academico.json` |
| O que está atrasado? | `atividades.json` |
| Qual tarefa devo priorizar? | `atividades.json`, `disciplinas.json`, `lembretes.json` |
| Tenho alguma DP cadastrada? | `disciplinas.json`, `atividades.json` |
| Quais matérias preciso estudar? | `disciplinas.json`, `atividades.json`, `observacoes.json` |

---

## 🧠 Estratégia de Integração

No protótipo inicial, os dados poderão ser carregados a partir de arquivos JSON armazenados na pasta `data/`.

A aplicação deverá:

1. Carregar os arquivos JSON ao iniciar.
2. Validar se os arquivos existem.
3. Usar listas vazias caso algum arquivo ainda não tenha dados.
4. Consultar as informações conforme a pergunta do usuário.
5. Retornar respostas apenas com base nos dados disponíveis.
6. Informar quando não houver informação suficiente.

---

## 🛡️ Regras Anti-Alucinação

O Flowup deverá seguir regras claras para evitar respostas inventadas.

### Regras principais

1. Não inventar provas, trabalhos, notas ou prazos.
2. Não criar disciplinas que não estejam cadastradas.
3. Não afirmar que uma tarefa está concluída sem registro do status.
4. Não dizer que há lembrete ativo se o lembrete não estiver registrado.
5. Quando não encontrar dados, informar a limitação.
6. Sugerir que o usuário cadastre ou revise as informações faltantes.

### Exemplo de resposta segura

```text
Não encontrei nenhuma prova cadastrada para esta semana.
Confira se todas as datas foram registradas corretamente no AcademyFLOW.
```

---

## 📌 Exemplo de Contexto Montado para o Agente

```text
Dados Acadêmicos do Estudante:

Disciplinas cadastradas:
- Engenharia de Software — status: em andamento
- Banco de Dados — status: em andamento

Atividades pendentes:
- Entrega da documentação do projeto — tipo: trabalho — data: 2026-05-15 — prioridade: alta
- Revisão para prova de Banco de Dados — tipo: revisão — data: 2026-05-18 — prioridade: média

Lembretes ativos:
- Revisar documentação do projeto — data: 2026-05-13 às 19:00

Observações recentes:
- O professor informou que a entrega poderá ser feita até sexta-feira.
```

---

## ✅ Resultado Esperado

Com uma base de conhecimento bem estruturada, o AcademyFLOW poderá oferecer respostas mais úteis, organizadas e confiáveis.

O agente Flowup não dependerá de suposições: ele deverá consultar os dados cadastrados e orientar o estudante com base nas informações reais disponíveis no sistema.
