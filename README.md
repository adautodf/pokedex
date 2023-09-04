# Entendendo como funciona o Protocolo HTTP

Documentação criada por Adauto Filho (@adautodf).

## Como funciona

URL: https://pokeapi.co/api/v2/pokemon \n
     ${Endereço IP} | ${patch = caminho de identificação do recurso}

## Tipos de Métodos Requisitados - API REST
O que a API irá nos entregar dependerá do tipo da requisição que estaremos solicitando.

## Request Method:
- GET -> Servidor entende que queremos Buscar Informação 
- POST -> Servidor entende que queremos Inserir Informação
- PUT -> Servidor entende que queremos Atualizar Informação
- DELETE -> Servidor entende que queremos Deletar Informação

## Formas iniciais de Passagem de Parâmetros para API
- Patch
- QueryString
- Header, "Metadados, Configurações da nossa requisição".
- Body

### Analisando Patch
```
"https://pokeapi.co/api/v2/pokemon/1
```
- O 1 representa um tipo de informação solicitada.

### Analisando QueryString
```
"https://pokeapi.co/api/v2/pokemon?offset=20&limit=20"
```
- Tudo que houver após o sinal de Interrogação (?), será a nossa QueryString. No caso citado, podemos ver que há dois.

## Analisando Headers
- Configuração da nossa API
### Request Headers (Cliente (Browser))
- Ele diz várias informações. Uma delas é o tipo de método, o accept (com os parâmetros definidos aceitos, mas não obrigatoriamente irá vir assim).
### Exemplo de informações:
- Credenciamento

```
Authorization: Bearer, Basic...
```

- Accept-language

```
pt-BR; q=1 (prioridade máxima de linguagem/tradução)
pt; q=0.9
en-US; q=0.8
en; q=0.7
gl; q=0.6 (prioridade "mínima")
```

### Response Headers (Servidor responde)

## Analisando Body
- Request Method (GET) não faz sentido
- Request Method (POST) faz sentido, se usaria o ```content-type: application/json``` no Request Headers.

## Status CODE
- Serve para dizer se nossa aplicação foi processada ou não.

### Famílias de Resposta | Códigos
- 100-199 -> Informativas
- 200-299 -> Bem-Sucedidas
- 300-399 -> Mensagem de Redirecionamento
- 400-499 -> Erro do cliente
- 500-599 -> Erro Interno do Servidor

# Em breve, continuação da documentação sobre o restante do Projeto.