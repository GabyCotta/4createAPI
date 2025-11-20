# API de Produtos

Estrutura simples em Flask para cadastro e listagem de produtos. Projeto utilizado em atividade de Sistemas Distribuídos e Mobile.

## Estrutura de Pastas

```
atv 4/
├── api.py                # Aplicação Flask principal
├── banco.py              # Conexão e funções de acesso ao banco SQLite
├── produtos.db           # Banco de dados local
├── templates/            # Páginas HTML renderizadas pelo Flask
│   ├── index.html        # Página inicial
│   ├── cadastrar.html    # Formulário de cadastro de produtos
│   └── listar.html       # Lista de produtos cadastrados
└── venv/                 # Ambiente virtual Python
```

## Rotas da API

### `GET /`
Retorna a página inicial.

### `GET /produtos/cadastrar`
Retorna o formulário HTML para cadastro.

### `POST /produtos/cadastrar`
Recebe JSON com `{ nome, preco }` e grava no banco.

### `GET /produtos`
Retorna lista de produtos cadastrados.

## Como executar

```bash
python api.py
```
A API inicia em:
```
http://127.0.0.1:5000
```

## Como testar no Postman

### POST `/produtos/cadastrar`
Body → JSON:
```json
{
  "nome": "Teclado",
  "preco": 150
}
```

### GET `/produtos`
Sem body.

## Requisitos
- Python 3.x
- Flask
- SQLite3

## Instalação
```bash
pip install flask
```
