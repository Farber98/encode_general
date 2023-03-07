# How to create Nest project using yarn

0. Init nest project with Typescript strict mode. Pick yarn as package manager.

```
nest new project-name --strict
```

1. If yarn failed inside project init, create yarn.lock and retry.
```
touch yarn.lock
yarn install
```

2. Install yarn dependencies for VScode. After they are installed, press Allow.
```
yarn dlx @yarnpkg/sdks vscode
```
