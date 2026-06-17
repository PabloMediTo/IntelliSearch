# Product Chatbot

An AI-powered product chatbot built with React, TypeScript, and Vite. Users can interact with a conversational interface to get information about products.

## Tech Stack

- **React 19** with TypeScript
- **Vite** for fast development and builds
- **React Markdown** for rendering formatted responses
- **ESLint** for code quality

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or higher)
- npm or yarn

### Installation

```bash
git clone https://github.com/<your-username>/IntelliSearch.git
cd IntelliSearch
npm install
```

### Development

```bash
npm run dev
```

### Build

```bash
npm run build
```

### Preview Production Build

```bash
npm run preview
```

### Lint

```bash
npm run lint
```

## Project Structure

```
src/
├── adapter/          # Chat adapter logic
├── api/              # Product API layer
├── assets/           # Static assets
├── components/       # React components (Chat, ChatInput, ChatMessage)
├── data/             # Product data
├── App.tsx           # Root component
├── types.ts          # TypeScript type definitions
└── main.tsx          # App entry point
```

## License

MIT
```

You can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...
      // Enable lint rules for React
      reactX.configs['recommended-typescript'],
      // Enable lint rules for React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```
