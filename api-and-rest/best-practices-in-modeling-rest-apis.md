# Boas práticas na Modelagem de API's REST

### Faça uso de recursos corretamente

- Use pronomes, e não verbos
- Não misture plural e singular

Ex:

Não use:

- `/getAllCars`
- `/createNewCar`
- `/deleteAllRedCars`

`/cars` ao invés de `/car`

`/users` ao invés de `/user`

### Utilize sub-recursos

Relacionamentos existentes devem estar explícitos na URL

Ex:

- Retorna uma lista de motoristas do carro 711:

  - **GET** `/cars/711/drivers`

- Retorna o motorista 4 do carro 711:
  - **GET** `/cars/711/drivers/4`

### Entenda sobre idempotência

<p align="center">
  <img 
    src="https://harshitjainhome.files.wordpress.com/2019/05/understanding-idempotency-and-safety-in-api-design.png" 
    alt="idempotency" 
    width="400"
  />
</p>

Idempotência é quando você realiza a mesma operação mais de uma vez, o resultado deve ser o mesmo.

Ex: Se eu busco todos os carros da minha frota três vezes, o resultado tem que ser o mesmo, ou seja, todos os carros da minha frota.

### Não ignore os cabeçalhos HTTP

Existem várias informações que podem (e devem) ser transmitidas através de cabeçalhos.

- `Content-Type`
- `Accept`
- `Cache`

Ex: Sempre informar o formato de dados que está devolvendo, JSON, XML ou HTML.

### Hypermedia as the engine of application state (HATEOAS) é assunto por si só, mas basicamente, facilita a interação com a API. Forneça links:

Ex:

```json
{
  "cursos": [
    {
      "id": 1,
      "nome": "C# (C Sharp)",
      "links": [
        {
          "type": "GET",
          "rel": "self",
          "uri": "api.treinaweb.com.br/cursos/1"
        },
        {
          "type": "GET",
          "rel": "curso_aulas",
          "uri": "api.treinaweb.com.br/cursos/1/aulas"
        }
      ]
    }
  ]
}
```

### Filtro, ordenação, paginação e seleção de campos

Sua API deve ser flexível:

- **GET** `/cars?color=red`
- **GET** `/cars?seats<=2`
- **GET** `/cars?sort=-manufactorer,+model`
- **GET** `/cars?fields=manufactorer, model, id, color`
- **GET** `/cars?offset=10&limit=5`

### Versione sua API

Alterações que demandam alteração no cliente DEVEM gerar uma nova versão da API

Ex:

- `blog/api/v1/posts?name=Título do post`
- `blog/api/v2/posts?title=Título do post`

### Utilize os status HTTP corretamente

<p align="center">
  <img 
    src="https://miro.medium.com/max/920/1*w_iicbG7L3xEQTArjHUS6g.jpeg" 
    alt="http status codes" 
    width="400"
  />
</p>
