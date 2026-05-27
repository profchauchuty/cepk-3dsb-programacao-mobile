# PARTE 2 — Partidas

# Atividade (AV1) - Programação Mobile

## Jogos Escolares - CEPK

---

# Objetivo

Desenvolver a estrutura de gerenciamento de partidas dos Jogos Escolares do CEPK.

Nesta etapa o aplicativo deverá possuir:
- CRUD de Partidas
- Controle de fases

---

# Tecnologias Obrigatórias

- React Native
- Expo Snack
- React Native Paper
- React Navigation
- JavaScript ou TypeScript

### Referências
- https://snack.expo.dev
- https://reactnative.dev
- https://reactnativepaper.com
- https://reactnavigation.org

---

# Funcionalidades Obrigatórias

## CRUD de Partidas

Cada partida deverá possuir:
- equipe A
- equipe B
- esporte
- modalidade
- fase
- data
- horário
- local

### Funcionalidades
- cadastrar
- listar
- editar
- excluir
- pesquisar

---

# Enum de Fases

Criar um enum para as fases:
- GRUPOS
- OITAVAS
- QUARTAS
- SEMIFINAL
- FINAL

---

# Estrutura Mínima do Projeto

```text
/projeto
│
├── App.js
│
├── /telas
│   │
│   ├── /dashboard
│   │   └── DashboardScreen.js
│   │
│   ├── /equipes
│   │   ├── EquipesScreen.js
│   │   ├── EquipeFormScreen.js
│   │   └── EquipeDetalhesScreen.js
│   │
│   └── /partidas
│       ├── PartidasScreen.js
│       ├── PartidaFormScreen.js
│       └── PartidaDetalhesScreen.js
│
├── /componentes
│   └── Cabecalho.js
│
├── /rotas
│   └── AppRotas.js
│
├── /database
│   └── db.js
│
├── /services
│   ├── EquipesService.js
│   └── PartidasService.js
│
├── /enums
│   ├── Esportes.js
│   ├── Modalidades.js
│   └── Fases.js
│
└── /assets
```

---

# Persistência em Memória

Os dados deverão ser armazenados em arrays dentro do arquivo `db.js`.

---
