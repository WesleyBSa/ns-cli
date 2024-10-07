# NS-CLI

A **NS-CLI** é um utilitário de linha de comando que permite buscar os endereços IP e os servidores de nomes (NS) de qualquer host na internet. Esta aplicação foi desenvolvida em Golang e utiliza a biblioteca [urfave/cli](https://github.com/urfave/cli) para a criação de comandos de terminal.

## Funcionalidades

- Buscar os endereços IP de um domínio.
- Buscar os servidores de nomes (NS) de um domínio.

## Tecnologias Utilizadas

![Golang](https://cdn.jsdelivr.net/gh/devicons/devicon/icons/go/go-original-wordmark.svg)

- **Golang**: Linguagem de programação utilizada para desenvolver a aplicação.
- **urfave/cli**: Biblioteca utilizada para criação da interface de linha de comando.

## Como utilizar

### Pré-requisitos

- [Golang](https://golang.org/doc/install) instalado na sua máquina.

### Instalação

Clone este repositório:

```bash
git clone https://github.com/WesleyBSa/ns-cli.git
cd ns-cli
```

Compile o projeto:

```bash
go build
```

### Executando a aplicação

A aplicação CLI possui dois comandos principais: `ip` e `servidores`. Você pode passar o nome do host como uma flag para buscar as informações.

#### Exemplo 1: Buscar IPs de um domínio

```bash
./cli ip --host mercadolivre.com.br
```

Isso exibirá todos os endereços IPs associados ao domínio `mercadolivre.com.br`.

#### Exemplo 2: Buscar servidores de nomes de um domínio

```bash
./cli servidores --host mercadolivre.com.br
```

Isso listará os servidores de nome (NS) do domínio `mercadolivre.com.br`.

### Flags

- `--host`: Define o domínio ou host a ser consultado. O valor padrão é `github.com/WesleyBSa`.

### Estrutura do Projeto

```bash
├── app/
│   └── app.go    # Lógica de busca de IPs e servidores
├── cmd/
│   └── main.go   # Ponto de entrada da aplicação
├── go.mod        # Módulo Go
└── go.sum        # Dependências do projeto
```
