# Bytebank Application

## Descrição
O Bytebank é uma aplicação de console desenvolvida em Java que simula operações bancárias básicas. A aplicação permite abrir e encerrar contas, consultar saldo, realizar saques, depósitos e transferências entre contas.

## Estrutura do Projeto

### Pacotes Principais
- `br.com.alura.bytebank`: Contém a classe principal da aplicação.
- `br.com.alura.bytebank.domain`: Contém as exceções e classes relacionadas ao domínio do negócio.
- `br.com.alura.bytebank.domain.cliente`: Contém classes relacionadas aos clientes.
- `br.com.alura.bytebank.domain.conta`: Contém classes relacionadas às contas e operações bancárias.

### Classes Principais
- `BytebankApplication`: Classe principal que inicializa a aplicação e gerencia o menu de operações.
- `ContaService`: Classe responsável pela lógica de negócio das operações bancárias.
- `ContaDAO`: Classe responsável pela persistência dos dados das contas no banco de dados.

## Funcionalidades

### Menu Principal
- Listar contas abertas
- Abrir conta
- Encerrar conta
- Consultar saldo
- Realizar saque
- Realizar depósito
- Realizar transferência
- Sair

### Detalhes das Operações

1. **Listar Contas**: Exibe todas as contas abertas no banco.
2. **Abrir Conta**: Permite a abertura de uma nova conta mediante o fornecimento de número da conta, nome, CPF e email do cliente.
3. **Encerrar Conta**: Encerra logicamente uma conta, desde que a mesma não possua saldo.
4. **Consultar Saldo**: Consulta o saldo disponível em uma conta específica.
5. **Realizar Saque**: Realiza um saque de um valor específico de uma conta, desde que a conta tenha saldo suficiente e esteja ativa.
6. **Realizar Depósito**: Realiza um depósito em uma conta.
7. **Realizar Transferência**: Transfere um valor de uma conta origem para uma conta destino, efetuando um saque na conta origem e um depósito na conta destino.
8. **Sair**: Encerra a aplicação.

## Como Executar

1. **Clone o repositório:**
   ```sh
   git clone https://github.com/seu-usuario/bytebank.git
   ```
2. **Navegue até o diretório do projeto:**
   ```sh
   cd bytebank
   ```
3. **Compile o projeto:**
   ```sh
   javac -d bin src/br/com/alura/bytebank/*.java src/br/com/alura/bytebank/domain/*.java src/br/com/alura/bytebank/domain/cliente/*.java src/br/com/alura/bytebank/domain/conta/*.java
   ```
4. **Execute a aplicação:**
   ```sh
   java -cp bin br.com.alura.bytebank.BytebankApplication
   ```

## Estrutura do Banco de Dados

### Tabela: `conta`
- `numero` (INT): Número da conta.
- `saldo` (DECIMAL): Saldo da conta.
- `cliente_nome` (VARCHAR): Nome do cliente.
- `cliente_cpf` (VARCHAR): CPF do cliente.
- `cliente_email` (VARCHAR): Email do cliente.
- `esta_ativa` (BOOLEAN): Status da conta (ativa/inativa).

## Exceções Tratadas
- `RegraDeNegocioException`: Exceção lançada para regras de negócio violadas, como saldo insuficiente, valor de saque/deposito inválido, conta inexistente, etc.


Caso tenha mais alguma coisa que gostaria de adicionar ou modificar, fique à vontade para me informar!
