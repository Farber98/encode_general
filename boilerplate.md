# How to create Hardhat project using yarn

0. Create project folder and get inside

```
mkdir project && cd project
```

1. Initialize yarn project

```
touch yarn.lock && yarn init -2
```

2. Get back node_modules, add hardhat dependencies and remove readme

```
yarn config set nodeLinker node-modules && yarn add hardhat --dev && rm README.md
```

3. Initialize hardhat project

```
yarn hardhat init
```

4. Rename tests and remove template files from contracts, scripts and tests.

```
mv test tests && rm contracts/* && rm -r scripts/* && rm -r tests/* && yarn hardhat clean
```

5. create .mocharc.json file

```
cat > .mocharc.json <<- "EOF"
{
"require": "hardhat/register",
"timeout": 40000,
"\_": ["tests/**/*.ts"]
}
EOF
```

6. Add properties to tsconfig.json

```
echo "$(jq '. += {"include": ["./scripts", "./tests", "./typechain-types"]}' tsconfig.json)" > tsconfig.json
echo "$(jq '. += {"files": ["./hardhat.config.ts"]}' tsconfig.json)" > tsconfig.json
```

7. create .env file

```
cat > .env <<- "EOF"
MNEMONIC=""
PRIVATE_KEY=""
INFURA_API_KEY=""
INFURA_API_SECRET=""
ALCHEMY_API_KEY=""
ETHERSCAN_API_KEY=""
EOF
```

8. Open project on vscode

```
code .
```

9. Add paths inside HardhatUserConfig at file hardhat.config.ts

```
...
const config: HardhatUserConfig = {
    paths: { tests: "tests" },
    ...
}
...

```
