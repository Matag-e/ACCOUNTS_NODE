# ACCOUNTS

Este projeto é um software simples desenvolvido em Node.js que simula as funcionalidades básicas de um banco. Utilizando as bibliotecas [Inquirer](https://www.npmjs.com/package/inquirer) e [Chalk](https://www.npmjs.com/package/chalk), o sistema permite ao usuário realizar operações bancárias como saques, depósitos, consultas de saldo e criação de novas contas.


## Tela inicial
![Interface](https://i.imgur.com/GfOQZ2X.png)


### 1. **Criar Nova Conta**
- O usuário pode criar uma nova conta fornecendo o nome da conta.
- As informações da conta são armazenadas em um arquivo JSON, criado através da função `buildAccount()` com auxilio do modulo [fs](https://www.npmjs.com/package/file-system).

Ao selecionar `Criar Conta` no console, ele te da a opção de digitar um nome para sua conta:

![createAccount](https://i.imgur.com/tlQcvEX.png)

E te retorna um aviso que a conta foi criada, a conta vem em formato `JSON` e  é criada em `accounts` localizada dentro da pasta raiz do projeto.

![](https://i.imgur.com/v3STG2x.png)


### 2. **Consultar Saldo**
- Permite ao usuário consultar o saldo da conta informando o nome da conta.

Após selecionar a ação de `Consultar Saldo`, é solicitado o nome da conta e te retornará o saldo da conta:

![](https://i.imgur.com/yi4KAR9.png)

### 3. **Realizar Depósito**
- O usuário pode realizar depósitos em uma conta existente.
- O valor depositado é adicionado ao saldo atual da conta.

Ao selecionar a ação de `Depositar`, é solicitado que coloque o nome da conta e o valor que você deseja depositar, ao inserir o valor e pressionar a tecla enter, você já tem o valor depositado como saldo da sua conta.

- **Tela depósito**

![deposit](https://i.imgur.com/Zm6mmEa.png)

- **Saldo após depósito**

![amount](https://i.imgur.com/WZgnuk7.png)

### 4. **Realizar Saque**
- O usuário pode realizar saques de uma conta existente.
- O valor sacado é subtraído do saldo da conta, desde que haja saldo suficiente.

Ao selecionar a opção `Sacar`, é solicitado que coloque o nome da conta e o valor que deseja sacar, mas o valor precisa conter em saldo na sua conta, caso não tenha, aparecerá um erro avisando que o saldo está indisponivel em sua conta bancaria.

- **Tela Saque**
  
![withdraw](https://i.imgur.com/Hm5YB2J.png)

- **Saldo Insuficiente**
 
![](https://i.imgur.com/UPoyBL3.png)

- **Saldo após saque**
  
![](https://i.imgur.com/TLxPIMM.png)

## Tecnologias Utilizadas

- **Node.js**: Ambiente de execução para JavaScript no servidor.
- **Inquirer**: Biblioteca para criar interfaces de linha de comando interativas.
- **Chalk**: Biblioteca para estilizar o texto no terminal.
