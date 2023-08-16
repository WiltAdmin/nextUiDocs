### [Installation](https://nextui.org/docs/frameworks/vite#installation)

In your Vite React project, run one of the following command to install NextUI:

```
npm i @nextui-org/react framer-motion
```

### [Tailwind CSS Setup](https://nextui.org/docs/frameworks/vite#tailwind-css-setup)

NextUI is built on top of Tailwind CSS, so you need to install Tailwind CSS first. You can follow the official [installation guide](https://tailwindcss.com/docs/guides/vite#react) to install Tailwind CSS. Then you need to add the following code to your `tailwind.config.js` file:

```
// tailwind.config.jsconst { nextui } = require("@nextui-org/react");/** @type {import('tailwindcss').Config} */module.exports = {  content: [    // ...    './node_modules/@nextui-org/theme/dist/**/*.{js,ts,jsx,tsx}'  ],  theme: {    extend: {},  },  darkMode: "class",  plugins: [nextui()]}
```

### [Provider Setup](https://nextui.org/docs/frameworks/vite#provider-setup)

After installing NextUI, you need to set up the `NextUIProvider` at the `root` of your application.

Go to the src directory and inside `main.jsx` or `main.tsx`, wrap `NextUIProvider` around App:

```
// main.tsx or main.jsximport React from 'react'import ReactDOM from 'react-dom/client'import {NextUIProvider} from '@nextui-org/react'import App from './App'import './index.css'ReactDOM.createRoot(document.getElementById('root')).render(  <React.StrictMode>    <NextUIProvider>      <App />    </NextUIProvider>  </React.StrictMode>,)
```

### [Setup pnpm (optional)](https://nextui.org/docs/frameworks/vite#setup-pnpm-optional)

If you are using pnpm, you need to add the following code to your `.npmrc` file:

```
public-hoist-pattern[]=*@nextui-org/theme*
```

After modfiying the `.npmrc` file, you need to run `pnpm install` again to ensure that the dependencies are installed correctly.