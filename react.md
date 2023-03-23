# How to create Typescript React project using yarn and Vite.

Create vite project
```
yarn create vite

Pick: React, Typescript.
```

Install dependencies with yarn using nodeLinker to node-modules
```
touch yarn.lock
yarn config set nodeLinker node-modules
yarn install
yarn add ethers@^5.7.2 --dev
```

Create components folder
```
mkdir src/components
```

Useful commands
```
yarn run dev
```
