# Módulo MongoDB![Mongo Icon](https://camo.githubusercontent.com/b543a486d75c07ba1660c64851a2fc7b94113774/687474703a2f2f7777772e6178616e747765622e636f6d2f696d616765732f69636f6e732f6d6f6e676f2e706e67) - Workshop Be MEAN

![Be Mean Icon](https://camo.githubusercontent.com/1a286c9f755fd3565a692c42b38c34495e44ac68/687474703a2f2f7765627363686f6f6c2e696f2f62656d65616e2f696d616765732f6c6f676f2e706e67)

***

###Sobre
[Link Oficial](http://dagora.net/be-mean/)

Workshop de [**MEAN**](http://mean.io/) ([MongoDb](https://www.mongodb.org/), [Express](http://expressjs.com/), [Angular](https://angularjs.org/) e [NodeJs](https://nodejs.org/en/) via CROWDFUNDING. Criação de um sistema Web Full Stack igual o Instagram utilizando somente **Javascript**.



##MongoDb![Mongo Icon](https://camo.githubusercontent.com/b543a486d75c07ba1660c64851a2fc7b94113774/687474703a2f2f7777772e6178616e747765622e636f6d2f696d616765732f69636f6e732f6d6f6e676f2e706e67)



O **MongoDb** é um banco e dados NoSQL open-source e orientado a documentos JSON.


##Links![Mongo Icon](https://camo.githubusercontent.com/b543a486d75c07ba1660c64851a2fc7b94113774/687474703a2f2f7777772e6178616e747765622e636f6d2f696d616765732f69636f6e732f6d6f6e676f2e706e67)


[Site Oficial](https://www.mongodb.org/)

[Be Mean - Repo Oficial](https://github.com/Webschool-io/be-mean-instagram)

[Aulas e Slides](https://github.com/Webschool-io/be-mean-instagram/wiki/M%C3%B3dulo-_--MongoDB)

[Chat](http://be-mean.rocket.chat/channel/mongodb)

[Artigos](https://github.com/Webschool-io/be-mean-instagram-artigos)

[mongo-hacker](https://github.com/TylerBrock/mongo-hacker)

#####Exercícios

[Wiki](https://github.com/Webschool-io/be-mean-instagram/wiki/Exerc%C3%ADcios)

* [Exercício 01](https://github.com/Webschool-io/be-mean-instagram/blob/master/apostila/classes/mongodb/class-01-resolved.md) - [Resolved](https://github.com/gabrieltome/be-mean-instagram-mongodb/blob/master/exercises/class-01-resolved-gabrieltome.md) 
* [Exercício 02](https://github.com/Webschool-io/be-mean-instagram/blob/master/apostila/classes/mongodb/class-02-resolved.md#estrutura) - [Resolved](https://github.com/gabrieltome/be-mean-instagram-mongodb-excercises/blob/master/class-02/class-02-resolved-gabrieltome.md)
* Exercício 03
* Exercício 04

***

##Workshop![Mongo Icon](https://camo.githubusercontent.com/b543a486d75c07ba1660c64851a2fc7b94113774/687474703a2f2f7777772e6178616e747765622e636f6d2f696d616765732f69636f6e732f6d6f6e676f2e706e67)


###Aula 01

Nessa primeira aula foi apresentado o **MongoDB**.

Starta o shell

```
mongo
```

Em outro terminal


```
mongod
```


Levantar já usando a database.

```
mongo database
```


**Export**

```
mongoexport --db nome_do_database --collection nome_da_colecao --out minha_colecao.json
```

**Import**

```
mongoimport --db nome_do_database --collection nome_da_colecao --drop --file minha_colecao.json
```

***

###Aula 02

Nessa aula foi mostrado alguns exemplos de CRUD.

A variável *db* sempre aponta para a database.


**Listar as databases**

```
show dbs
```

**Seleciona banco**

Especifica qual banco de dados a ser utilizado.
Se não existir, ele cria o banco.

```
use datababe
```

**Lista as coleções do db**

```
show collections
```


####CRUD

**Insert**

```
db.collection.insert()
```

A primeira inserção é mais demorada, pois o **MongoDb** pré-aloca espaço na memória.


```                 
db.teste.insert({nome:"Gabriel", idade:"26"})

Inserted 1 record(s) in 1663ms
WriteResult({
  "nInserted": 1
})
```

**Save**

Insere salva.

- Cria o objeto a ser salvo
  	
  	```
  	var obj = {"name":'Name'}
  	```
- Salva passando o objeto como parâmetro
	
	```
	db.collection.save(obj)
	```

**FIND**

Retorna o ***CURSOR***

```
db.collection.find()
```

Retorna o ***OBJETO***

Salva a busca

```
var query = {name:'Name'}
```
 e depois

```
var p = db.collection.findOne(query)
```




###Aula 03
###Aula 04






