# todo

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn run serve
```

### Compiles and minifies for production
```
yarn run build
```

### Run your tests
```
yarn run test
```

### Lints and fixes files
```
yarn run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


## Steps:
initial scafold
  $ vue create todo

quick test
  $ cd todo
  $ yarn serve

hit http://localhost:8080/

create remote git repo and copy setup commands:
  $ git remote add origin https://github.com/<your-user-name>/<your-repo>.git
  $ git push -u origin master

add vuetify
  $ vue add vuetify

check it
  $ yarn serve

commit and push to github
  $ git status
  $ git add -A .
  $ git commit -m 'add vuetify'
  $ git push

open editor
  $ code .

## Things to do:

-  shift list card up closer to header
-  add new todo input field
-  wire up add button
-  add complete and delete buttons to each item
