# React, Next, TypeScriptのManual Setting

## Package Manager: yarn
```
$ brew install yarn
$ yarn init
```

## Language: TypeScript, JavaScript
```
$ touch tsconfig.json
$ yarn add typescript @types/node
```
```:tsconfig.json
{
    "compilerOptions": {
        "target": "ES2015",
        "module": "commonjs",
        "strict": true,
        "jsx": "preserve",
        "esModuleInterop": true,
        "skipLibCheck": true,
        "forceConsistentCasingInFileNames": true
    },
    "include": ["**/*.ts", "**/*.tsx"],
    "exclude": ["node_modules"]
}
```

## JavaScript Library: React
```
$ yarn add react react-dom @types/react
```

## Building Tool: Next.js
[src](https://nextjs.org/docs/getting-started)
```
$ yarn add next
$ mkdir pages
$ touch pages/index.tsx
```

`package.json`に付け足す。
```:json
"scripts": {
  "dev": "next dev",
  "build": "next build",
  "start": "next start",
  "lint": "next lint"
}
```

`pages/index.tsx`の内容
```:index.tsx
import React from 'react'

const IndexPage = () => {
  return <div>Hello, World!</div>
}

export default IndexPage
```

start develop
```
$ yarn dev
```

## Version Management System: Git

ignore `.next/` folder
```
$ touch .gitignore
$ echo ".next" >> .gitignore
$ echo "node_modules/**" >> .gitignore
```

access `localhost:3000`

## Hosting Tool: Vercel
https://vercel.com/new
