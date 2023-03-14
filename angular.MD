# How to create Angular project using npm

1. Install angular
```
npm install -g @angular/cli
```

2. Create angular project
```
ng new my-project

Pick: no, scss
```

Pack, build and serve angular
```
npm start
```

Install dependencies
```
npm i ethers@^5.7.2
npm install bootstrap
npm i @popperjs/core
```

To use bootstrap, edit style key in angular.json file
```
"styles": [
  "src/styles.scss",
  "node_modules/bootstrap/dist/css/bootstrap.min.css"
],
```

To use bootstrap, edit scripts key in angular.json file
```
"scripts": [
  "node_modules/bootstrap/dist/js/bootstrap.bundle.min.js"
]
```
To use json abi, edit tsconfig.json and inside compiler options:
```
  "resolveJsonModule": true,
  "allowSyntheticDefaultImports": true,
```


