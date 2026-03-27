# 🚀 API ZelaCidade

## 📍 Sobre o prejeto

A API **ZelaCidade** foi criada para registrar e gerenciar problemas urbanos, como:

- Buracos
- Vazamentos
- Lixo
- Iluminação

Essa API nos permite criar, visualizar, atualizar e deletar ocorrências.

## 🛠️ Tecnologias utilizadas

- Node.js
- Express
- SQLite
- SQLite3
- Postman
- Nodemon

---

## 📦 Instalação

`npm istall`

---

## ▶️ Como executar

```bash
npm run dev
```

`http://localhost:3000`

[Clique Aqui](http://localhost:3000)

---

## 🗄️ Banco de Dados

O banco de dados é criado automaticamente ao iniciar o prejeto.

```
database.db
```

## 📃 Tabela

|Campo           |Descrição                |
|----------------|-------------------------|
|id              |Identificador único      |
|tipo_problema   |Tipo do problema         |
|localizacao     |Onde ocorreu             |
|descricao       |Detalhes do incidente    |
|prioridade      |Baixa, Média ou Alta     |
|data_registro   |Data do registro         |
|hora_registro   |Hora do registro         |
|status_resolucao|Status (Padrão: Pendente)|

---

## 🔗 Endpoints
### Rota inicial

```http
GET /
```
Retorna uma página HTML simples com informações da API.

---

### Rota para listar todos os incidentes

```http
GET /incidentes
```
Retorna todos os registros do banco de dados.

---

### Rota para buscar um incidente específico (ID)

```http
GET /incidentes/:id
```
 Ex: /incidenets/1

Retorna uma ocorrência específica.

---

### Rota para criar um novo incidente

```http
POST /incidentes
```

Body (JSON)

```json
{
        "id": 1,
        "tipo_problema": "Iluminação",
        "localizacao": "Rua das Flores, 123, Bairro das Margaridas",
        "descricao": "Poste queimado há dias",
        "prioridade": "Média",
        "nome_solicitante": "Ana Clara",
        "data_registro": "16/03/2026",
        "hora_registro": "10:30",
        "status_resolucao": "Em Análise"
    }
```

---

### Rota para atualizar um incidente

```json
PUT /incidentes/:id
```

Body (JSON)

```json
{
        "descricao": "Luz do poste foi trocada",
        "prioridade": "Baixa",
        "status_resolução": "Resolvido"
    }
```

## 🔒 Segurança
A API utiliza `?` nas queries SQL:

```sql
WHERE id = ?
```
Isso evita o SQL Injection.

---

## 📚 Conceitos

- CRUD (Create, Read, Update e Delete)
- Rotas com Express

---

## 👩‍💻 Projeto educacional
Este projeto foi desenvolvido para fins de aprendizado em back-end com Node.js.