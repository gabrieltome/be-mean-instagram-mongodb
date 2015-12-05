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

__[Official Manual](https://docs.mongodb.org/manual/)__

[Classes Slides](https://github.com/Webschool-io/be-mean-instagram/wiki/M%C3%B3dulo-_--MongoDB)

[Chat](http://be-mean.rocket.chat/channel/mongodb)

[Articles](https://github.com/Webschool-io/be-mean-instagram-artigos)

[mongo-hacker](https://github.com/TylerBrock/mongo-hacker)

#####Exercícios

[Wiki](https://github.com/Webschool-io/be-mean-instagram/wiki/Exerc%C3%ADcios)

* [Exercise 01](https://github.com/Webschool-io/be-mean-instagram/blob/master/apostila/classes/mongodb/class-01-resolved.md) - [Resolved](https://github.com/gabrieltome/be-mean-instagram-mongodb/blob/master/exercises/class-01-resolved-gabrieltome.md) 
* [Exercise 02](https://github.com/Webschool-io/be-mean-instagram/blob/master/apostila/classes/mongodb/class-02-resolved.md#estrutura) - [Resolved](https://github.com/gabrieltome/be-mean-instagram-mongodb-excercises/blob/master/class-02/class-02-resolved-gabrieltome.md)
* [Exercise 03](https://github.com/Webschool-io/be-mean-instagram/blob/master/apostila/classes/mongodb/class-03-resolved.md) - [Resolved](https://github.com/gabrieltome/be-mean-instagram-mongodb/blob/master/exercises/class-03-resolved-gabrieltome.md)
* Exercise 04

***

##Workshop![Mongo Icon](https://camo.githubusercontent.com/b543a486d75c07ba1660c64851a2fc7b94113774/687474703a2f2f7777772e6178616e747765622e636f6d2f696d616765732f69636f6e732f6d6f6e676f2e706e67)


###Class 01

In this first class the was showed the MongoDB and some important features.

Starts the shell

```
mongo
```

In other terminal window

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

###**Insert/CREATE**

#####Syntax

```
db.collection.insert()
```

(traduzir)
The first insert is the slower because **MongoDb** pre allocates memory space.


```                 
db.teste.insert({nome:"Gabriel", idade:"26"})

Inserted 1 record(s) in 1663ms
WriteResult({
  "nInserted": 1
})
```

###**SAVE**

####Insert and Save

- Create the object to save
  	
  	```
  	var obj = {"name":'Name'}
  	```
  	
- Saves parsing the object by param	
	
	```
	db.collection.save(obj)
	```

####**Find**

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

---


###Class 03

####_id UUID

Example of UUID

```
 ObjectId("565d08724a4eb81c28471da7")
```

###**Retrieve**

####Query


Find two params

```
db.collection.find({clausulas},{fields})
```

###OperadoresAritméticos

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

####Existential Operator


Search the objects **that have** field

#####Syntax
```
db.collection.find({field: {$exists:true}})
```
Return the object if field exists


---

###Class 04 - pt 1


###UPDATE


The function **update()** takes three parameters

- _query_
- _modification_
- _options_

#####Syntax


```
db.collection.update(query, mod, options)
```


###Mod Operators

####$set

The __$set__ operator modifies a value, if doesn't exists, it's created.

#####Syntax

```
{ $set: { field: value } }
```

######Example

```
db.pokemons.update({name: 'Pikachu'}, {$set: {attack: 100}})
```

######Other example with "_id" in *query*


```
var mod = {$set: {name:'Brutal', attack:10000, defense:10000,height:10,description:'Pokemon de teste'}}

var query = {"_id": ObjectId("565d08724a4eb81c28471da7")}

db.pokemons.update(query, mod)
```

####$unset

**Excludes** fields JSON document.

#####Syntax

```
var mod = {$unset: {field: 1}}
db.collection.update(query, mod)
```

######Example

```
var mod = {$unset: {height:1}}
db,pokemons.update(query, mod)
```

####$inc

The **$inc** operator increases a desired amount in the field.
If field don't exists, the field is created with the value inside.

#####Syntax

```
var mod = {$inc: { field: 1}}
db.collections.update(query, mod)
```

#####Example

**+10**

```
var mod = {$inc: {attack: 10}}
db.pokemons.update)(query, mod)
```

#####To **DECREASE**

**-10**


```
var mod = {$inc: {attack: -10}}
db.pokemons.update)(query, mod)
```

###**ARRAY** Operators


####$push

The **$push** operator puts a value in the array's field.

If the field doesn't exists, a new array field is created with the value inside.

If the field exists but don't is an array, returns a error.

#####Syntax

```
{ $push: { field : value }}
```

#####Example

```
var mod = {$push: {moves: 'Choque do Trovão'}}
db.pokemons.update(query, mod)
```

####$pushAll

The **$pushAll** operator puts __*each*__ value of the **_[Array_of_values]_** in the array's field.

If the field doesn't exists, a new array field is created with the value inside.

If the field exists but don't is an array, returns a error.

#####Syntax

```
{ $pushAll: { field : [Array_of_values] }}
```

#####Example

```
var attacks = ['Choque do Trovão','Investida','Ataque Rápido']
var mod = {$pushAll: {moves, attacks}}
db.pokemons.update(query, mod)
```

####$pull

The $pull operator removes the value of the array field.

If doesn't exists, nothing is done.

If the field exists but don't is an array returns a error.

#####Syntax

```
{$pull : { field : value}}
```

#####Example


```
var mod = {$pull: {moves: 'Ataque Rápido'}}
db.pokemons.update(query, mod)
```

####$pullAll

The **$pullAll** operator **REMOVES** **EACH** value of the **_[Array_of_values]_** in the array's field.

If doesn't exists, nothing is done.

If the field exists but don't is an array, returns a error.

#####Syntax

```
{ $pullAll: { field : [Array_of_values] }}
```

#####Example

```
var attacks = ['Investida','Ataque Rápido']
var mod = {$pullAll: {moves, attacks}}
db.pokemons.update(query, mod)
```

### Options do update()

####update() - options

The **options** object will be used to setup some different values for the standard update.

#####Syntax

```
{
	upsert: boolean,  <-
	multi: boolean,
	writeConcern: document
}
```

####update() - options - upsert

If the document is not found by the query, it inserts the object that is being sent by the modifier. 

The standard is FALSE.

#####Syntax

```
var query = {field: /sometext/i}
var mod = {$set: {active: true}}
var options = {upsert: true}
db.collectins.update(query, mod, options)
```

#####Example

```
var query = {name: /Pikachu/i}
var mod = {$set: {active:true}}
var options = {upsert: true}
db.pokemons.update(query, mod, options)
```

####update() - options - upsert - $setOnInsert


The **$setOnInsert** set the values will be that added only if happen a **upset**.

#####Syntax with example


```
var query = {name: /NãoExisteMon/i}
var mod = { 
	$set: {active:true},
	$setOnInsert{ 
	name:"NaoExisteMon",
	attack:null,
	defense:null,
	height:null,
	description:"Sem maiores infos"}
	}
var options = {upsert: true}
db.pokemons.update(query, mod, options)

```

####update() - options - multi

MongoDb allows you to change only one document at a time.

If we want to change more than one document, we must set the parameter like **TRUE**.

#####Syntax

```
var query = {}
var mod = {$set: {field:value}}
var options = {multi:true}
db.collection.update(query, mod, options)
```

#####Example

```
var query = {}
var mod = {$set: {active:false}}
var options = {multi:true}
db.pokemons.update(query, mod, options)

// 8 docs changed

Updated 8 existing record(s) in 7ms
WriteResult({
  "nMatched": 8,
  "nUpserted": 0,
  "nModified": 8
})
```

####update() - options - writeConcern

**WriteConcern** describes the assurance of that MongoDB gives success relate of the write operation.


###More of Array Operators

####find() - Operador de Array - $in

 **$in** returns the documents that has some value into [Array Of Values].

#####Syntax

```
{field: {$in: [Array_of_values]}}
db.collection.find(query)
```

#####Example

```
var query = {moves: {$in: [/choque do trovão/i]}}
db.pokemons.find(query)
```

####find() - Operador de Array - $nin

Not in.

Reverse of the $in.

The $nin returns documents if no values are found.


#####Syntax

```
{field: {$nin: [Array_of_values]}}
db.collection.find(query)
```

#####Example

```
var query = {moves: {$nin: [/choque do trovão/i]}}
db.pokemons.find(query)
```


####find() - Operador de Array - $all

Like an **AND**.

Return documents if ALL the values are found.

#####Syntax

```
{field: {$all: [Array_of_values]}}
db.collection.find(query)
```

#####Example

```
var query = {moves: {$all: ['investida','hidro bomba']}}
db.pokemons.find(query)
```

###Negation Operators


####find() - Operador de Negação - $ne

**NOT EQUAL**

#####Syntax

```
{field: {$ne: value}}

```

#####Example

```
var query = {type: {$ne: 'Water'}}
db.pokemons.find(query)
```

**DON'T REGEX!!!!**


####find() - Operador de Negação - $ne

**REGEX OK!!**

#####Syntax

```
{field: {$not: value}}
db.collection.find(query)
```

#####Example

```
var query = {name: {$not: /pikachu/i}}
db.pokemons.find(query)
```

###DELETE

###remove()

#####Syntax

```
var query = {field: value}
db.collection.remove(query)
```

#####Example

```
var query = {name: /Magikarp/i}
db.pokemons.remove(query)
```