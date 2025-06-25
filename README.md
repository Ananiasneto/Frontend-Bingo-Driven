## Link deploy :

https://frontend-bingo-driven.vercel.app/

## 1. Criar uma network Docker (opcional)

Se quiser que seu frontend se comunique com outros containers (ex: backend), crie uma network Docker:

```bash
docker network create minha-network
```

## 2. Construir a imagem do frontend

No diretório do frontend (onde está o Dockerfile), execute:

```bash
docker build -t myfrontend .
```

---

## 3. Executar o container do frontend

```bash
docker run -d \
  --name NOMECONTAINER \
  --network NOMENETWORK \
  -p 3000:80 \
  myfrontend
```

---

# Rodar a aplicação com Docker Compose

No terminal, no mesmo diretório do `docker-compose.yml`, execute:

```bash
docker compose up -d --build
```


## Parar a aplicação

Para derrubar os containers criados pelo Compose:

```bash
docker compose down
```

## Considerações finais
---

- O frontend ficará disponível em `http://localhost:3000`.

---
