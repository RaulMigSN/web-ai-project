
---

# Projeto Web de Salas de Áudio

Este projeto é uma aplicação web que permite a criação de salas, envio e gravação de perguntas em áudio. O objetivo é proporcionar um ambiente onde usuários possam criar salas temáticas, gravar áudios diretamente do navegador e interagir com a Inteligência Artificial Gemini de forma simples e eficiente, onde ela se baseará no áudio gravado na página.

---

## 🛠️ Tecnologias Utilizadas

- **React** (com TypeScript): Biblioteca principal para construção da interface.
- **Vite**: Ferramenta de build e desenvolvimento rápido.
- **React Router**: Gerenciamento de rotas/páginas.
- **Day.js**: Manipulação de datas.
- **Fetch API**: Comunicação HTTP com backend.
- **CSS**: Estilização customizada.

---

## 🚧 O que foi construído

- **Criação de salas**: Usuários podem criar novas salas para organizar discussões ou temas.
- **Listagem de salas**: Visualização de todas as salas disponíveis.
- **Envio de perguntas**: Usuários podem enviar perguntas para uma sala específica.
- **Listagem de perguntas**: Visualização das perguntas enviadas em cada sala.
- **Gravação de áudio**: Usuários podem gravar áudios diretamente do navegador e enviar para uma sala.
- **Componentização**: Interface dividida em componentes reutilizáveis para formulários, listas, itens e elementos de UI.

---

## 📄 Páginas

As páginas principais estão localizadas em `src/pages/`:

- **create-room.tsx**: Página para criação de novas salas.
- **room.tsx**: Página de visualização de uma sala específica e suas perguntas.
- **record-room-audio.tsx**: Página para gravação e envio de áudios para uma sala.

---

## 🧩 Componentização

Os componentes reutilizáveis estão em `src/components/`:

- **Formulários**:
  - `create-room-form.tsx`: Formulário para criar salas.
  - `question-form.tsx`: Formulário para enviar perguntas.
- **Listagens**:
  - `room-list.tsx`: Lista de salas disponíveis.
  - `question-list.tsx`: Lista de perguntas de uma sala.
  - `question-item.tsx`: Item individual de pergunta.
- **UI (Interface de Usuário)**:
  - `badge.tsx`, `button.tsx`, `card.tsx`, `form.tsx`, `input.tsx`, `label.tsx`, `textarea.tsx`: Componentes de interface reutilizáveis para padronizar a experiência do usuário.

---

## 📦 Tipos (Types)

Os tipos TypeScript para requisições e respostas HTTP estão em `src/http/types/`:

- **create-room-request.ts** / **create-room-response.ts**: Tipos para criação de sala.
- **create-question-request.ts** / **create-question-response.ts**: Tipos para criação de perguntas.
- **get-rooms-response.ts**: Tipos para listagem de salas.
- **get-room-questions-response.ts**: Tipos para listagem de perguntas de uma sala.

---

## 🔗 Serviços HTTP

Os hooks para comunicação com o backend estão em `src/http/`:

- **use-create-room.ts**: Hook para criar uma nova sala.
- **use-rooms.ts**: Hook para buscar salas existentes.
- **use-create-question.ts**: Hook para criar uma nova pergunta.
- **use-room-questions.ts**: Hook para buscar perguntas de uma sala.

---

## 🎤 Gravação de Áudio

A página `record-room-audio.tsx` permite gravar áudios diretamente do navegador (usando a API `MediaRecorder`) e enviá-los para o backend via `FormData`. A gravação é segmentada em blocos de 5 segundos para facilitar o envio e processamento.

---

## 🚀 Como rodar o projeto

1. Instale as dependências:
   ```bash
   npm install
   ```
2. Inicie o servidor de desenvolvimento:
   ```bash
   npm run dev
   ```
3. Acesse no navegador: [http://localhost:5173](http://localhost:5173)

---

## 📁 Estrutura de Pastas

```
<code_block_to_apply_changes_from>
src/
  app.tsx
  main.tsx
  index.css
  components/
    create-room-form.tsx
    question-form.tsx
    question-item.tsx
    question-list.tsx
    room-list.tsx
    ui/
      badge.tsx
      button.tsx
      card.tsx
      form.tsx
      input.tsx
      label.tsx
      textarea.tsx
  http/
    types/
      create-question-request.ts
      create-question-response.ts
      create-room-request.ts
      create-room-response.ts
      get-room-questions-response.ts
      get-rooms-response.ts
    use-create-question.ts
    use-create-room.ts
    use-room-questions.ts
    use-rooms.ts
  lib/
    dayjs.ts
    utils.ts
  pages/
    create-room.tsx
    record-room-audio.tsx
    room.tsx
```

---

## ✨ Observações

- O projeto é totalmente componentizado, facilitando a manutenção e evolução.
- Os tipos TypeScript garantem segurança nas integrações com o backend.
- A gravação de áudio utiliza recursos nativos do navegador, sem dependências externas.

---
