# MongoDB Blog Project

Este projeto é uma aplicação RESTful que simula um blog, utilizando **Spring Boot** e **MongoDB**. Ele permite gerenciar usuários, postagens e comentários, demonstrando as funcionalidades do MongoDB para armazenamento de dados não-relacionais, incluindo a persistência de objetos aninhados e referências entre documentos.

---

## 💻 Tecnologias Utilizadas

Este projeto foi desenvolvido utilizando as seguintes tecnologias:

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-F2F4F9?style=for-the-badge&logo=spring-boot)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![Git Bash](https://img.shields.io/badge/Git%20Bash-F05032?style=for-the-badge&logo=git&logoColor=white)

---

## 🔑 Funcionalidades e Modelagem de Dados

### Classes Principais

* **`User`**: Representa um usuário do blog. Possui atributos como nome e e-mail. Um usuário pode ter várias postagens (`posts`).
* **`Post`**: Representa uma postagem no blog. Contém o título, o corpo do texto e a data. É associada a um `User` (autor) e pode conter uma lista de `comments`.
* **`CommentDTO`**: Objeto de transferência de dados para os comentários. Armazena o texto do comentário, a data e o autor.

### Repositórios e Consultas Avançadas

O projeto utiliza o **Spring Data MongoDB** para interagir com o banco de dados. O `PostRepository` demonstra o uso de **consultas personalizadas** (`@Query`) para buscar postagens:

* **`searchTitle`**: Encontra postagens cujo título corresponde a um determinado texto, ignorando maiúsculas e minúsculas.
* **`fullSearch`**: Uma consulta complexa que busca postagens por texto no título, corpo ou comentários, em um intervalo de datas especificado.

---
Banco de Dados MongoDB em Execução

A imagem abaixo mostra a base de dados workshop_mongo rodando no MongoDB Compass, com as coleções post e user, exibindo documentos e seus relacionamentos.











---

## 📁 Como Rodar o Projeto

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)
    ```
2.  **Configure o MongoDB:** Certifique-se de ter uma instância do MongoDB rodando localmente ou altere a configuração no `application.properties` para se conectar a um banco de dados remoto.
3.  **Execute a classe `WorkshopmongoApplication`** no seu ambiente de desenvolvimento (ex: IntelliJ, VS Code).
4.  Use o Postman para testar os endpoints da API.

---

## 🤝 Contribuições

Este projeto está aberto a contribuições. Sinta-se à vontade para abrir uma *issue* ou enviar um *pull request*.

---

## ✉️ Contato

Guilherme Vieira - gv524003@gmail.com
