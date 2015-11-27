# Módulo MongoDB![Mongo Icon](https://camo.githubusercontent.com/b543a486d75c07ba1660c64851a2fc7b94113774/687474703a2f2f7777772e6178616e747765622e636f6d2f696d616765732f69636f6e732f6d6f6e676f2e706e67) - Workshop Be MEAN

![Be Mean Icon](https://camo.githubusercontent.com/1a286c9f755fd3565a692c42b38c34495e44ac68/687474703a2f2f7765627363686f6f6c2e696f2f62656d65616e2f696d616765732f6c6f676f2e706e67)

***

###Sobre
[Link Oficial](http://dagora.net/be-mean/)

Workshop de [**MEAN**](http://mean.io/) ([MongoDb](https://www.mongodb.org/), [Express](http://expressjs.com/), [Angular](https://angularjs.org/) e [NodeJs](https://nodejs.org/en/) via CROWDFUNDING. Criação de um sistema Web Full Stack igual o Instagram utilizando somente **Javascript**.



##MongoDb![Mongo Icon](https://camo.githubusercontent.com/b543a486d75c07ba1660c64851a2fc7b94113774/687474703a2f2f7777772e6178616e747765622e636f6d2f696d616765732f69636f6e732f6d6f6e676f2e706e67)

[traduzir] 
O **MongoDb** é um banco de dados NoSQL open-source e orientado a documentos JSON.


##Links![Mongo Icon](https://camo.githubusercontent.com/b543a486d75c07ba1660c64851a2fc7b94113774/687474703a2f2f7777772e6178616e747765622e636f6d2f696d616765732f69636f6e732f6d6f6e676f2e706e67)


[Official Website](https://www.mongodb.org/)

[Be Mean - Official Repository](https://github.com/Webschool-io/be-mean-instagram)

[Classes Slides](https://github.com/Webschool-io/be-mean-instagram/wiki/M%C3%B3dulo-_--MongoDB)

[Chat](http://be-mean.rocket.chat/channel/mongodb)

[Articles](https://github.com/Webschool-io/be-mean-instagram-artigos)

[mongo-hacker](https://github.com/TylerBrock/mongo-hacker)

#####Exercícios

[Wiki](https://github.com/Webschool-io/be-mean-instagram/wiki/Exerc%C3%ADcios)

* [Exercise 01](https://github.com/Webschool-io/be-mean-instagram/blob/master/apostila/classes/mongodb/class-01-resolved.md) - [Resolved](https://github.com/gabrieltome/be-mean-instagram-mongodb/blob/master/exercises/class-01-resolved-gabrieltome.md) 
* [Exercise 02](https://github.com/Webschool-io/be-mean-instagram/blob/master/apostila/classes/mongodb/class-02-resolved.md#estrutura) - [Resolved](https://github.com/gabrieltome/be-mean-instagram-mongodb-excercises/blob/master/class-02/class-02-resolved-gabrieltome.md)
* Exercise 03
* Exercise 04

***

##Workshop![Mongo Icon](https://camo.githubusercontent.com/b543a486d75c07ba1660c64851a2fc7b94113774/687474703a2f2f7777772e6178616e747765622e636f6d2f696d616765732f69636f6e732f6d6f6e676f2e706e67)


###Class 01

In this first class the was showed the MongoDB and some important features.

Starts the shell

```
mongo
```

Other term

```
mongod
```

[traduzir]
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

###Class 02

This class show some examples of CRUD.

The *db var* always target 4 the database.

**List the databases**

```
show dbs
```

**Select the database**

Pick the database from the server.

If don't exists, it's create the database

```
use datababe
```

**List the Collections from database**

```
show collections
```


####CRUD

**Insert**

```
db.collection.insert()
```

(traduzir)
A primeira inserção é mais demorada, pois o **MongoDb** pré-aloca espaço na memória.


```                 
db.teste.insert({nome:"Gabriel", idade:"26"})

Inserted 1 record(s) in 1663ms
WriteResult({
  "nInserted": 1
})
```

**Save**

Insert and Save

- Create the object to save
  	
  	```
  	var obj = {"name":'Name'}
  	```
  	
- Saves parsing the object by param	
	
	```
	db.collection.save(obj)
	```

**FIND**

Return the ***CURSOR***

```
db.collection.find()
```

Return a ***OBJECT***

Save the search


```
var query = {name:'Name'}
```

and after

```
var p = db.collection.findOne(query)
```




###Class 03

####_id UUID

##Retrieve

####Query


Find two params

```
db.collection.find({clausulas},{fields})
```

##OperadoresAritméticos

####< is $lt - less than

```
db.collection.find({ "field" : { $lt: value } } );
```
Retorna objetos com valores menores que *value*.


####<= is $lte - less than or equal


```
db.collection.find({ "field" : { $lte: value } } );
```
Retorna objetos com valores maiores ou igual a *value*.



####> is $gt - greater than


```
db.collection.find({ "field" : { $gt: value } } );
```
Retorna objetos com valores maiores que *value*.


####>= is $gte - greater than or equal

```
db.collection.find({ "field" : { $gte: value } } );
```
Retorna objetos com valores maiores ou igual a *value*.


###Operadores Lógicos


####$or

Recebe dois arrays

```
var query = { $or : [{a:1},{b:2}]}
db.collection.find(query)
```

####$nor
Negação do *$or*

```
var query = { $or : [{a:1},{b:2}]}
db.collection.find(query)
```

####$and

```
var query = { $or : [{a:1},{b:2}]}
db.collection.find(query)
```

####Operador existêncial

(Melhorar)

Search the objects that have field

```
db.collection.find({field: {$exists:true}})
```
Return the object if field exists



###Aula 04


####Operador de Array






