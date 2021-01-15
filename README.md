# osworks-api
API Spring Rest (Curso Spring AlgaWorks)


### Configurações:
 - Java 11
 - Spring
 - MySQL
 
URL: http://localhost
PORT: 8080

## _Cliente_

GET `/clientes`
GET `/clientes/{clienteId}`
POST `/clientes`
PUT /clientes/{clienteId}`
DELETE `/clientes/{clienteId}`


- RESPONSE
```json
[
  {
    "id": 1,
    "nome": "Brunno Sena",
    "email": "brunnow@hotmail.com",
    "telefone": "51 99706-3185"
  },
  ...
]
```

- REQUEST
```json 
{
	"nome": "Isaias",
	"email": "isaias@email.com",
	"telefone": "51 998989-262362"
}
```



## _OrdemServico_

POST `/ordens-servico`
GET `/ordens-servico`
GET `/ordens-servico/{id}`
GET `/ordens-servico/{id}/comentarios`
POST `/ordens-servico/{id}/comentarios`
PUT `/ordens-servico/{id}/finalizacao`


- REQUEST
```json 
{
	"cliente": {
		"id": 1
	},
	"descricao": "pc com problema",
	"preco": 190.20
}
```


- RESPONSE
```json
[
  {
    "id": 1,
    "cliente": {
      "id": 1,
      "nome": "Brunno Sena"
    },
    "descricao": "reparo de notebook, cliente diz que não liga",
    "preco": 300.20,
    "status": "ABERTA",
    "dataAbertura": "2021-01-14T16:13:11-03:00",
    "dataFinalizacao": null
  },
  ...
```
