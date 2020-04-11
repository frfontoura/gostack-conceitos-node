# Desafio 02: Conceitos do Node.js

Este é um desafio do GoStack Bootcamp da RocketSeat. [Link para o desafio](https://github.com/Rocketseat/bootcamp-gostack-desafios/tree/master/desafio-conceitos-nodejs)

Essa é uma aplicação para armazenar repositórios do seu portfólio, que permite a criação, listagem, atualização e remoção dos repositórios, e além disso permite que os repositórios possam receber "likes".

Os serviços disponíveis são:

| URL                    | Method | Descrição                                 | Request                                                                                   | Response                                                                                                        |
|------------------------|--------|-------------------------------------------|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| /repositories          | POST   | Permite a criação de um novo repositório  | { title: 'Desafio Node.js', url: 'http://github.com/...', techs: ["Node.js", "..."] }     | { id: "uuid", title: 'Desafio Node.js', url: 'http://github.com/...', techs: ["Node.js", "..."], likes: 0 }     |
| /repositories          | GET    | Rota que lista todos os repositórios      |                                                                                           | [{ id: "uuid", title: 'Desafio Node.js', url: 'http://github.com/...', techs: ["Node.js", "..."], likes: 0 }]   |
| /repositories/:id      | PUT    | Permite a alteração do title, url e techs | { title: 'Desafio Node.js', url: 'http://github.com/...', techs: ["Node.js", "ReactJs"] } | { id: "uuid", title: 'Desafio Node.js', url: 'http://github.com/...', techs: ["Node.js", "ReactJs"], likes: 0 } |
| /repositories/:id      | DELETE | Remove um repositório da lista            |                                                                                           | { id: "uuid", title: 'Desafio Node.js', url: 'http://github.com/...', techs: ["Node.js", "..."], likes: 1 }     |
| /repositories/:id/like | POST   | Soma +1 aos 'likes' do repositório        |                                                                                           |                                                                                                                 |


## Requisitos

* NodeJs - (desenvolvido utilizando a versão v12.16.2)
* Yarn - (opcional - versão 1.17.3)

## Instalação

1 - Fazer o gitclone:

```
git clone https://github.com/frfontoura/gostack-conceitos-node
```

2 - Instalar as dependências:
```
yarn
```

3 - Inicializar o servidor:
```
yarn dev
```

## Executando os testes

Para executar os testes, utilizar o comando:
```
yarn test
```