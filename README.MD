# Minimal API Fórmula 1

Este projeto é uma API simples construída usando Fastify para fornecer informações sobre as equipes e pilotos de Fórmula 1. A API suporta CORS e permite que os usuários obtenham detalhes sobre equipes e pilotos através de vários endpoints.

## Índice

- [Instalação](#instalação)
- [Uso](#uso)
- [Endpoints da API](#endpoints-da-api)
  - [GET /teams](#get-teams)
  - [GET /drivers](#get-drivers)
  - [GET /drivers/:id](#get-driversid)
  - [GET /teams/:id](#get-teamsid)
- [Scripts](#scripts)
- [Dependências](#dependências)
- [Licença](#licença)

## Instalação

1. Clone o repositório:

   ```bash
   git clone https://github.com/yuridiasp/minimal-api-f1.git
   ```

2. Navegue até o diretório do projeto:

   ```bash
   cd minimal-api-f1
   ```

3. Instale as dependências:

   ```bash
   npm install
   ```

## Uso

### Desenvolvimento

Para iniciar o servidor em modo de desenvolvimento, execute o seguinte comando:

```bash
npm run start:dev
```

O servidor será iniciado e ouvirá na porta `3333`. Você pode acessar a API em `http://localhost:3333`.

### Produção

Para iniciar o servidor em modo de produção, execute os seguintes comandos:

```bash
npm run dist
npm run start:dist
```

## Endpoints da API

### GET /teams

Obtém a lista de todas as equipes de Fórmula 1.

- **URL:** `/teams`
- **Método:** `GET`
- **Resposta:**
  ```json
  {
    "teams": [
      { "id": 1, "name": "Mclaren", "base": "Woking, United Kingdom" },
      { "id": 2, "name": "Mercedes", "base": "Brackley, United Kingdom" },
      ...
    ]
  }
  ```

### GET /drivers

Obtém a lista de todos os pilotos de Fórmula 1.

- **URL:** `/drivers`
- **Método:** `GET`
- **Resposta:**
  ```json
  {
    "drivers": [
      { "id": 1, "name": "Max Verstappen", "team": "Red Bull Racing" },
      { "id": 2, "name": "Lewis Hamilton", "team": "Mercedes" },
      ...
    ]
  }
  ```

### GET /drivers/:id

Obtém os detalhes de um piloto específico pelo seu ID.

- **URL:** `/drivers/:id`
- **Método:** `GET`
- **Parâmetros de URL:** `id` - ID do piloto
- **Resposta:**
  ```json
  {
    "driver": {
      "id": 1,
      "name": "Max Verstappen",
      "team": "Red Bull Racing"
    }
  }
  ```
  ou
  ```json
  {
    "message": "Driver not found"
  }
  ```

### GET /teams/:id

Obtém os detalhes de uma equipe específica pelo seu ID.

- **URL:** `/teams/:id`
- **Método:** `GET`
- **Parâmetros de URL:** `id` - ID da equipe
- **Resposta:**
  ```json
  {
    "team": {
      "id": 1,
      "name": "Mclaren",
      "base": "Woking, United Kingdom"
    }
  }
  ```
  ou
  ```json
  {
    "message": "Team not found"
  }
  ```

## Scripts

- `dist`: Compila o código TypeScript para JavaScript.
- `start:dev`: Inicia o servidor em modo de desenvolvimento com recarregamento automático.
- `start:watch`: Inicia o servidor em modo de desenvolvimento com observação de arquivos.
- `start:dist`: Compila o código e inicia o servidor em modo de produção.

## Dependências

- Produção:
  - `@fastify/cors`: ^9.0.1
  - `fastify`: ^4.27.0

- Desenvolvimento:
  - `@types/cors`: ^2.8.17
  - `@types/node`: ^20.11.30
  - `tsup`: ^8.0.2
  - `tsx`: ^4.7.1
  - `typescript`: ^5.4.3

## Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## Desenvolvedor

<p>
    <a href="https://github.com/yuridiasp">
        <img
          align=left
          margin=10
          width=80
          src="https://avatars.githubusercontent.com/u/81938754?v=4"
        />
    </a>
      <p>
        <p>&nbsp&nbsp<a style="color: white;" href="https://github.com/yuridiasp">Yuri Dias</a><br>
        &nbsp&nbsp&nbsp
    </p>
</p>

<br>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/yuridiasp/) [![Discord](https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white)](https://discord.com/channels/@yuridiasp/) [![Facebook](https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white)](https://www.facebook.com/yuri.dias.7739/) [![X](https://img.shields.io/badge/X-000?style=for-the-badge&logo=x)](https://x.com/YuriDias_P) [![Instagram](https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/yuridiasp/) [![E-mail](https://img.shields.io/badge/-Email-000?style=for-the-badge&logo=microsoft-outlook&logoColor=007BFF)](mailto:yuristardias@hotmail.com)