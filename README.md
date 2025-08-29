# Desafio MBA Engenharia de Software com IA - Full Cycle

## Como executar a solução

### 1. Pré-requisitos
- Python 3.10 ou superior
- Docker e Docker Compose

### 2. Instalação das dependências

Execute o comando abaixo na raiz do projeto:

```
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### 3. Configuração do ambiente

Crie um arquivo `.env` na raiz do projeto com as variáveis de ambiente necessárias (exemplo: chaves de API, configurações de banco de dados, etc).

```
GEMINI_API_KEY=CHANGE_ME
DATABASE_URL=postgresql+psycopg://postgres:postgres@localhost:5434/rag
PG_VECTOR_COLLECTION_NAME=desafio01
PDF_PATH=document.pdf
```

### 4. Ordem de execução

1. Suba o banco de dados vetorial utilizando o Docker Compose:

	```
	docker compose up -d
	```

2. Execute a ingestão do PDF:

	```
	python src/ingest.py
	```

3. Rode o chat:

	```
	python src/chat.py
	```

Siga as instruções exibidas no terminal para interagir com o chat.

---

IMPORTANTE! Adapte as variáveis de ambiente e configurações conforme necessário para o seu ambiente.