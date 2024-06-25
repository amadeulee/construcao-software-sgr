# Projeto 01 - Entrega versão revisada

## Software para Gestão de Restaurantes 🥘🍳🔥

- Versão 1.0
- Engenharia de Software
- Construção de Software - 2024.01

## Entrega da versão revisada do projeto

**Instituto de Informática/UFG**

**Curso:** Engenharia de Software

**Professor:** Elias Batista Ferreira

**Alunos:**

- Amadeu Lee;
- Arthur Faria Peixoto;
- João Gabriel Cavalcante França;
- Leonardo Moreira de Araújo;
- Luca Santos Martins.

## Introdução

O projeto consiste em um sistema de gerenciamento de pedidos em um restaurante, facilitando as operações cotidianas dentro desse ambiente. Diversas ações estão contempladas, tais como anotar pedidos digitalmente, encaminhar pedidos para a cozinha, modificar o status dos pedidos, imprimir o pedido digitalmente, fechar contas de mesas, calcular lucros em intervalos determinados, acompanhar pedidos atribuídos a garçons e monitorar o estoque de ingredientes necessários para a preparação dos pratos.

Dentro do sistema, há a distinção entre dois tipos de funcionários responsáveis pelas principais operações: o garçom e o gerente. Enquanto o garçom concentra-se nas atividades diretas relacionadas aos pedidos, como a anotação e o encaminhamento dos pedidos, o fechamento das contas, entre outras, o gerente desempenha, além das funções do garçom, o controle do estoque do restaurante. Portanto, cabe ao gerente, quando identificada a demanda por algum ingrediente em estoque, providenciar a compra e a reposição do item. Em situações de alta demanda ou falta de pessoal, o gerente pode assumir as responsabilidades de um garçom, garantindo assim a continuidade das operações do restaurante.

## **Diagrama de classe:**

![image](https://github.com/amadeulee/construcao-software-sgr/assets/62031286/c37551b0-2db6-489b-9fec-17fd1d5aebaf)


- PedidoStatus:

  - Status do pedido do cliente, pendente, em preparo, pronto e entregue

- Pedido:

  - Classe que diz respeito ao pedido propriamente dito, ele tem uma lista de pedidos com todos os itens solicitados, o status do pedido e a mesa que pediu

- Mesa:

  - Classe que possuí somente o id da mesa (o código de identificação dela) e um booleano dizendo se ela está livre ou ocupada

- ItemPedido:

  - Classe referente ao Item do pedido do cliente. Ex: 1-Guaraná; 2-Coxinha. Possuí o atributo Item (referente ao item propriamente dito) e o atributo quantidade (quantas coxinhas o cliente pediu, por exemplo)

- Item:

  - Classe que refere ao item solicitado pelo cliente. Ex: X-bacon. Possuí o nome, o preço do pedido e uma lista com todos os ingredientes necessários para preparar o item.

- ItemIngrediente:

  - Classe que contém o nome do ingrediente e a quantidade (em gramas para comida e em quantidade para bebidas)

- Funcionario:

  - Classe que possuí os dados do funcionário (seja garçom, seja estoquista)

- Estoque:

  - Classe que possuí uma lista com todos os ingredientes existentes em estoque, cada item possuí um nome e a quantidade (atributos da classe estoqueIngrediente)

- estoqueIngrediente:
  - Classe que possuí o nome do ingrediente e a quantidade existente em estoque

## [História de Usuário](https://github.com/amadeulee/construcao-software-sgr/blob/master/SGR%20-%20Hist%C3%B3rias%20de%20Usu%C3%A1rio.pdf)

## [Casos de Testes](https://github.com/amadeulee/construcao-software-sgr/blob/master/SGR%20-%20Casos%20de%20Teste.pdf)

<!-- ## Gerencia de configuração: ❓ -->

## Endpoints:

### CRUD dos Garçons (Funcionário)

1. Criar Garçom

- Método: POST
- URL: http://localhost/api/garcons
- Body:

```
{
  "nome": "String",
  "cpf": "String",
  "email": "String",
  "idade": "Integer",
  "telefone": "String"
}

```

2. Obter Todos os Garçons

- Método: GET
- URL: http://localhost/api/garcons

3. Obter Garçom por ID

- Método: GET
- URL: http://localhost/api/garcons/{id}

4. Atualizar Garçom

- Método: PUT
- URL: http://localhost/api/garcons/{id}
- Body:

```
{
  "nome": "String",
  "cpf": "String",
  "email": "String",
  "idade": "Integer",
  "telefone": "String"
}

```

5. Excluir Garçom

- Método: DELETE
- URL: http://localhost/api/garcons/{id}

### CRUD dos Pedidos

1. Criar Pedido

- Método: POST
- URL: http://localhost/api/pedidos
- Body:

```
{
  "itensPedidos": [{"item": "ItemID", "quantidadeSolicitada": "Integer"}],
  "statusPedido": "PENDENTE",
  "mesa": "MesaID",
  "funcionario": "FuncionarioID"
}

```

2. Obter Todos os Pedidos

- Método: GET
- URL: http://localhost/api/pedidos

3. Obter Pedido por ID

- Método: GET
- URL: http://localhost/api/pedidos/{id}

4. Atualizar Pedido

- Método: PUT
- URL: http://localhost/api/pedidos/{id}
- Body:

```
{
  "itensPedidos": [{"item": "ItemID", "quantidadeSolicitada": "Integer"}],
  "statusPedido": "PedidoStatus",
  "mesa": "MesaID",
  "funcionario": "FuncionarioID"
}
```

5. Excluir Pedido

- Método: DELETE
- URL: http://localhost/api/pedidos/{id}

### CRUD dos Itens do Cardápio

1. Criar Item

- Método: POST
- URL: http://localhost/api/itens
- Body:

```
{
  "nome": "String",
  "preco": "Double",
  "itensIngredientes": [{"ingrediente": "IngredienteID", "quantidade": "Double"}]
}

```

2. Obter Todos os Itens

- Método: GET
- URL: http://localhost/api/itens

3. Obter Item por ID

- Método: GET
- URL: http://localhost/api/itens/{id}

4. Atualizar Item

- Método: PUT
- URL: http://localhost/api/itens/{id}
- Body:

```
{
  "nome": "String",
  "preco": "Double",
  "itensIngredientes": [{"ingrediente": "IngredienteID", "quantidade": "Double"}]
}

```

5. Excluir Item

- Método: DELETE
- URL: http://localhost/api/itens/{id}

### CRUD dos Ingredientes

1. Criar Ingrediente

- Método: POST
- URL: http://localhost/api/ingredientes
- Body:

```
{
  "nome": "String",
  "quantidade": "Double"
}
```

2. Obter Todos os Ingredientes

- Método: GET
- URL: http://localhost/api/ingredientes

3. Obter Ingrediente por ID

- Método: GET
- URL: http://localhost/api/ingredientes/{id}

4. Atualizar Ingrediente

- Método: PUT
- URL: http://localhost/api/ingredientes/{id}
- Body:

```
{
  "nome": "String",
  "quantidade": "Double"
}
```

5. Excluir Ingrediente

- Método: DELETE
- URL: http://localhost/api/ingredientes/{id}

### Endpoint Controle de Estoque

1. Obter Estoque

- Método: GET
- URL: http://localhost/api/estoque

### Endpoint para Controle de Mesas

1. Obter Todas as Mesas

- Método: GET
- URL: http://localhost/api/mesas

2. Obter Mesa por ID

- Método: GET
- URL: http://localhost/api/mesas/{id}

3. Atualizar Disponibilidade da Mesa

- Método: PUT
- URL: http://localhost/api/mesas/{id}
- Body:

```
{
  "livre": "boolean"
}
```

### Fechamento de Contas e Cálculo de Vendas

1. Fechar Conta por Mesa

- Método: POST
- URL: http://localhost/api/contas/fechar
- Body:

```
{
  "mesaId": "Integer"
}
```

2. Calcular Total de Vendas por Garçom

- Método: GET
- URL: http://localhost/api/vendas/garcom/{garcomId}

3. Calcular Total de Vendas em um Período

- Método: GET
- URL: http://localhost/api/vendas/periodo
- Parâmetros:
  - dataInicio: String (formato: YYYY-MM-DD)
  - dataFim: String (formato: YYYY-MM-DD)
