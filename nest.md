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

3. Make tsconfig.json resolveJsonModule
```
echo "$(jq '.compilerOptions += {"resolveJsonModule": true}' tsconfig.json)" > tsconfig.json
```

4. Install other dependencies
```
yarn add @nestjs/swagger && yarn add @nestjs/config && yarn add joi && yarn add ethers@^5.7.2
```

5. Remove prettier
```
yarn remove prettier

rm .prettierrc
```

6. Run command to update CLI commands.
```
yarn run
```

7. Start server in development mode
```
yarn start:dev
```
