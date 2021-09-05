## Aula 12 - Banco de Dados

![gifdatabase](<iframe src="https://giphy.com/embed/pOEbLRT4SwD35IELiQ" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/tech-technology-mograph-pOEbLRT4SwD35IELiQ">via GIPHY</a></p>)

O desafio era criar um banco de dados, para isso utilizei o comando abaixo:

* Criação de base de dados vendas
Utilizei o comando use vendas

* Inserção de documentos
 Primeiro criei uma nova collection utilizando o comando db.createcollection('vendedores')
 
Segundo no robô 3t utilizei o comando insert documents e colei os 5 Jsons de vendas.


* Atualização de documentos
Na collection vendedores update documents, inseri a informação da torre do vendedor
com o comando abaixo:

```

db.getCollection('vendedores').update(
    { "vendedor.nome" : "Sulamita" },
    { $set:
        { 
            "torre": 05 
        }
    }
);

```


* Exclusão de documentos

```
db.getCollection('vendedores'). remove({"vendedor.nome":"Aline"})
```

* Consulta com projeção
```

db.getCollection('vendedores').find({}, {"categoria":1})
```

* Consulta utilizando combinação entre os seletores

```
db.Collection('vendedores').sort({"produto.valor": 1, "cliente.torre": -1})
```

* Consulta paginada e ordenada (utilizar *skip*, *limit* e *sort*)
```
db.vendedores.find().limit(3)

db.vendedores.find().skip(4)

db.vendedores.find().sort({"cliente.nome":1})

```




