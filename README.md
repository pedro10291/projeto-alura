# Servidor Node.js Basic

import express from "express"

const app = express();
app.listen(3000, () =>{

    console.log("Servidor escutando...");
});

app.get("/api", (req, res) => {

    res.status(200).send("Olá, mundo.");
});

app.get("/livro", (req, res) =>{
       const livro = {
       
        titulo: "O Senhor dos Anéis",
        autor: "J.R.R. Tolkien",
        ano: 1954,
        genero: "Fantasia"
    };
    
    res.json(livro);  
});

**Descrição:**
Este é um simples servidor Node.js criado com Express.js que oferece duas rotas:
* `/api`: Retorna uma mensagem de saudação.
* `/livro`: Retorna informações sobre um livro em formato JSON.

**Tecnologias:**
* Node.js
* Express.js

**Instalação:**
1. Clone este repositório: `git clone https://github.com/seu_usuario/seu_repositorio.git`
2. Instale as dependências: `npm install`   


**Uso:**
1. Execute o servidor: `node index.js` (substitua `index.js` pelo nome do seu arquivo principal)
