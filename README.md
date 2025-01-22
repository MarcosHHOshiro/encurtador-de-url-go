# URL Shortener API

Este projeto é uma API simples de encurtador de URLs construída em Go utilizando a biblioteca **go-chi** para roteamento e middleware.

## Funcionalidades

- **Encurtar URL**: Recebe uma URL e retorna um código curto associado a ela.
- **Redirecionamento**: Dado um código curto, redireciona o cliente para a URL original.
- **Validação de URL**: Garante que as URLs recebidas sejam válidas.
- **Logs Estruturados**: Utiliza `slog` para registrar eventos relevantes.

## Tecnologias Utilizadas

- [Go](https://golang.org/)
- [go-chi/chi](https://github.com/go-chi/chi) - Para roteamento e middlewares.
- [math/rand/v2](https://pkg.go.dev/math/rand) - Para geração de códigos aleatórios.
- [slog](https://pkg.go.dev/log/slog) - Para logs estruturados.

## Endpoints

### **POST** `/api`
- **Descrição**: Encurta uma URL fornecida.
- **Corpo da Requisição**:
  ```json
  {
    "url": "https://example.com"
  }
-Resposta esperada:
  ```json
  {
    "url": "https://example.com"
  }

### **GET** `/{code}`
- **Descrição**: Redireciona para a URL original associada ao código curto fornecido.