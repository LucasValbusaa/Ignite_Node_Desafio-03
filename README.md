<h2 align="center">Desafio 02 🚀</h2>
<h5 align="center">Ignite - <a href="https://rocketseat.com.br/" >Rocketseat</a> - Trilha Node js</h5>

## 💻 Descrição

Desenvolver um CRUD de repositórios de projetos. Além disso, é possível dar likes em repositórios cadastrados, aumentando a quantidade de likes em 1 a cada vez que a rota é chamada.

## 🛠️ Funcionalidades

- Criar um repositórios com `title`, `url`, `techs`.
- Lista os repositório criados.
- Alterar o repositórios passando `id`.
- Excluir repositório passando `id`.
- Dar um like no repositório passando `id`.

## 🔗 Rotas

- POST `/repositories` → criar um novo `respositório`.

```javascript
//Exemplo de dados a serem enviados
{
	"title": "Umbriel",
	"techs": ["React", "ReactNative", "TypeScript", "ContextApi"],
	"url": "https://github.com/Rocketseat/umbriel"
}

//Exemplo de retorno
{
  "id": "7d455d24-314d-4570-9e23-e4fe699ac9ea",
  "title": "Umbriel",
  "url": "https://github.com/Rocketseat/umbriel",
  "techs": [
    "React",
    "ReactNative",
    "TypeScript",
    "ContextApi"
  ],
  "likes": 0
}
```

- GET `/repositories` → procura todos os `repositórios` criados.

```javascript
//Exemplo de retorno
[
  {
    id: "7d455d24-314d-4570-9e23-e4fe699ac9ea",
    title: "Umbriel",
    url: "https://github.com/Rocketseat/umbriel",
    techs: ["React", "ReactNative", "TypeScript", "ContextApi"],
    likes: 0,
  },
];
```

- PUT `/repositories/:id` → alterar o `title` e `ulr` do `techs` do `repositório` pasasndo um `id`.

```javascript
//Exemplo de dados a serem enviados
{
  "id": "7d455d24-314d-4570-9e23-e4fe699ac9ea",
  "title": "crud-repositories--02",
  "url": "https://github.com/Rocketseat/crud-repositories--02",
  "techs": [
    "TypeScript",
    "Prisma",
    "Jest"
  ],
  "likes": 0
}
```

- DELETE `/repositories/:id` → deleta um repositório passando `id`.

```javascript
// Sem conteúdo de retorno apenas status 204 de confirmação
```

- POST `/repositories/:id/like` → adiciona um like toda vez que a rota é chamada a um `respositório` passando `id`.

````javascript
//Exemplo de retorno
{
  "likes": 1
}


### 📝 Clonagem e uso

```bash
   #Clone
   git clone https://github.com/LucasValbusaa/Ignite_Node_Desafio-03.git

   #Install dependencies
   yarn

   #Run server
   yarn dev

   #Run tests
   yarn test
````
