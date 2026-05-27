# PARTE 1 — Dashboard + Equipes

# Atividade (AV1) - Programação Mobile

## Jogos Escolares - CEPK

---

# Objetivo

Desenvolver a estrutura inicial de um aplicativo mobile para gerenciamento dos Jogos Escolares do CEPK.

Nesta etapa o aplicativo deverá possuir:
- Dashboard
- Navegação
- CRUD de Equipes

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

## Dashboard

A tela inicial deverá apresentar:
- menu de navegação
- total de equipes
- total de jogadores
- total de partidas
- próximos jogos

---

## CRUD de Equipes

Cada equipe deverá possuir:
- nome
- esporte
- modalidade
- técnico/responsável
- logo/imagem
- jogadores

### Funcionalidades
- cadastrar
- listar
- editar
- excluir
- pesquisar

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
│   └── /equipes
│       ├── EquipesScreen.js
│       ├── EquipeFormScreen.js
│       └── EquipeDetalhesScreen.js
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
│   └── EquipesService.js
│
├── /enums
│   ├── Esportes.js
│   └── Modalidades.js
│
└── /assets
```

---

# Persistência em Memória

Os dados deverão ser armazenados em arrays dentro do arquivo `db.js`.

---
