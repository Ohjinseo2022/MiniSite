# frontend

## Project setup

```
npm install
```

### Compiles and hot-reloads for development

```
npm run serve
```

### Compiles and minifies for production

```
npm run build
```

### Lints and fixes files

```
npm run lint
```

###

.prettierrc 설정

{
"semi": false,
"bracketSpacing": true,
"singleQuote": true,
"useTabs": false,
"trailingComma": "none",
"printWidth": 80
}

기본 탬플릿 설정
"Generate Basic Vue Code": {
"prefix": "vue-start",
"body": [
"<template>\n\t<div></div>\n</template>\n<script>\nexport default {\n\tcomponents:{},\n\tdata() {\n\t\treturn {\n\t\t\tsampleData:''\n\t\t}},\n\tsetup() {},\n\tcreated() {},\n\tmounted() {},\n\tunmounted() {},\n\tmethods: {}\n}\n</script>"
],
"description": "Generate Basic Vue Code"
}

package.json -> rules 에 추가
"space-before-function-paren": "off",
"vue/multi-word-component-names": 0

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).
