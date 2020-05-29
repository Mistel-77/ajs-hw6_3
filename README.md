# ajs-hw6_3
Домашнее задание к лекции «Прототипы, конструкторы» JSDoc

[![Build status](https://ci.appveyor.com/api/projects/status/msb7b29fcktxbo4e/branch/master?svg=true)](https://ci.appveyor.com/project/Mistel-77/ajs-hw6-3/branch/master)

## JSDoc (задача со звёздочкой)

**Важно**: данная задача не является обязательной 

### Легенда

Как только вы приступаете к решению вопросов организации своего кода, жёстко встаёт вопрос о его документировании для участников вашей команды. Для этого есть много инструментов, но вы ваш выбор остановился на [JSDoc](http://usejsdoc.org).

### Описание JSDoc

Установите JSDoc в вашей проект с помощью следующей команды:
`npm install --save-dev jsdoc`

Создайте конфигурационный файл JSDoc - jsdoc.conf.json:
```json
{
  "source": {
    "include": ["src/js"]
  },
  "opts": {
    "encoding": "utf8",
    "destination": "docs",
    "recurse": true
  }
}
```
Создайте файл character.js с вашим приложением в каталоге js. В нём расположите заглушку функции:
```javascript
/**
 * <Общее описание>
 * 
 * @param <описание параметра>
 * @param <описание параметра>
 * 
 * @throws <описание генерируемой ошибки>
 */ 
function Character(name, type) {
  this.name = name;
  this.type = type;
}
```

Задайте скрипт npm в package.json:
`"doc": "jsdoc -c jsdoc.conf.json"`


Задокументируйте поведение функции-конструктора Character с использованием следующих doc-комментариев:
1. @param {<тип>} <имя> - описание параметра (см. [документацию](http://usejsdoc.org/tags-param.html))
1. @throws {<тип>} - описание генерируемого исключения (см. [документацию](http://usejsdoc.org/tags-throws.html))

Удостоверьтесь, что документация генирируется, запустив:
`npm run doc`

Добавьте каталог docs в .gitignore.
