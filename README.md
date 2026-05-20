# Delta Estoque

Sistema de controle de estoque desenvolvido com PHP e MySQL, permitindo cadastrar, listar, editar e excluir produtos de forma simples e intuitiva.

## Funcionalidades

- **Cadastro de produtos** — registra código, nome, quantidade, volume, fornecedor, preço e imagem
- **Listagem com busca** — exibe todos os produtos em cards e permite busca por código, nome ou fornecedor
- **Edição e exclusão** — edita os dados de qualquer produto ou o remove do estoque
- **Validação dupla** — validação no cliente (JavaScript) e no servidor (PHP)
- **Log de erros** — erros são registrados automaticamente em `erros-a1/erros.log`

## Tecnologias

| Camada | Tecnologia |
|--------|-----------|
| Backend | PHP (PDO) |
| Banco de dados | MySQL / MariaDB |
| Frontend | HTML5, CSS3, JavaScript |
| Ícones | Font Awesome 4.7 e 6.5 |
| Fonte | Google Fonts — Poppins |

## Pré-requisitos

- PHP 7.4 ou superior
- MySQL 5.7 ou superior (ou MariaDB equivalente)
- Servidor web com suporte a PHP (Apache, Nginx ou XAMPP/WAMP)

## Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/controle-de-estoque.git
   ```

2. Mova a pasta para o diretório do seu servidor web (ex: `htdocs` no XAMPP).

3. Importe o banco de dados:
   ```bash
   mysql -u root -p < database.sql
   ```

4. Configure a conexão com o banco em `conexao-db.php`:
   ```php
   $pdo = new PDO('mysql:host=localhost;dbname=delta_estoque', 'seu_usuario', 'sua_senha');
   ```

5. Acesse `http://localhost/controle-de-estoque` no navegador.

## Estrutura do Projeto

```
Controle de Estoque/
├── index.php            # Roteador principal
├── pagina-inicial.php   # Página de boas-vindas
├── cadastrar.php        # Formulário de cadastro de produto
├── listagem.php         # Listagem e busca de produtos
├── editar.php           # Edição e exclusão de produto
├── conexao-db.php       # Configuração da conexão com o banco
├── database.sql         # Schema do banco de dados
├── erros-a1/
│   ├── erros.log        # Log de erros da aplicação
│   └── script.js        # Validações client-side
├── imagens/             # Assets de imagem
└── esboco-telas/        # Mockups da interface (Excalidraw)
```

## Banco de Dados

O banco `delta_estoque` contém a tabela `produtos`:

| Coluna | Tipo | Descrição |
|--------|------|-----------|
| `id_produto` | INT (PK) | Identificador único |
| `codigo` | INT | Código do produto |
| `nome` | VARCHAR(100) | Nome do produto |
| `quantidade` | INT | Quantidade em estoque |
| `volume` | INT | Volume / tamanho |
| `fornecedor` | VARCHAR(100) | Nome do fornecedor |
| `valor` | DECIMAL(10,2) | Preço do produto |
| `image_url` | VARCHAR(255) | Caminho da imagem |

## Screenshots

> Adicione prints das telas aqui após subir o projeto.

## Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
