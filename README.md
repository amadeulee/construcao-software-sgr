# Documentação - API

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

O projeto consiste em um sistema de gerenciamento de pedidos em um restaurante, facilitando as operações cotidianas dentro desse ambiente. Diversas ações estão contempladas, tais como anotar pedidos digitalmente, modificar o status dos pedidos, imprimir o pedido digitalmente, fechar contas de mesas, calcular lucros em intervalos determinados, acompanhar pedidos atribuídos a garçons e monitorar o estoque do estabelecimento.

Dentro do sistema, há a distinção entre dois tipos de funcionários responsáveis pelas principais operações: o garçom e o gerente. Enquanto o garçom concentra-se nas atividades diretas relacionadas aos pedidos, como a anotação e o controle dos pedidos, o fechamento das contas, entre outras, enquanto isso, o gerente desempenha a parte relacionada ao controle de estoque, financeiro e das estatísticas do restaurante. Portanto, cabe ao gerente, quando identificada a falta de algum produto em estoque, providenciar a compra e a reposição do item.

## [História de Usuário](https://github.com/amadeulee/construcao-software-sgr/blob/master/SGR%20-%20Hist%C3%B3rias%20de%20Usu%C3%A1rio.pdf)

## **Diagrama de classe**

![image](https://github.com/amadeulee/construcao-software-sgr/blob/1663359318979e4a67579ef226a56b1a963890d5/Diagrama%20de%20Classes.png)

- StatusAtendimento
  
  - Enum que possui o status do atendimento do cliente, podendo ser: aberto ou finalizado
    
- Atendimento
  
  - Classe que possuí as características gerais do atendimento do cliente, possuindo informações como: o status do atendimento, o garçom responsável pela mesa, o valor gasto e o id da mesa 
    
- PedidoStatus:

  - Enum que possui o status do pedido do cliente, podendo ser: pendente, em preparo, pronto e entregue

- Mesa:

  - Classe que possuí somente o id da mesa (o código de identificação dela) e um booleano dizendo se ela está livre ou ocupada

- Funcionário:

  - Classe que possuí os dados do funcionário (nome, cpf, email, idade, telefone)

- Pedido:

  - Classe que diz respeito ao pedido propriamente dito, ele tem uma lista de pedidos com todos os itens solicitados, o status do pedido, a mesa que pediu e o funcionário responsável pelo atendimento

- ItemVenda:

  - Classe que refere ao item solicitado pelo cliente. Ex: X-bacon. Possuí o nome, o preço do pedido e uma lista com todos os ingredientes necessários para preparar o item

- Estoque:

  - Classe que possuí uma lista com todos os ingredientes existentes em estoque, cada item possuí um nome e a quantidade (atributos da classe ItemEstoque)

- ItemEstoque:
  
  - Classe que possuí o nome do ingrediente e a quantidade existente em estoque, podendo essa ser inteira e/ou fracionada
  
- TipoMovimentação:
  
  -  Enum que possui os tipos de movimentações que podem ser realizadas no estoque, sendo "entrada" ou "saída" de itens
     
## [Casos de Testes](https://github.com/amadeulee/construcao-software-sgr/blob/master/SGR%20-%20Casos%20de%20Teste.pdf)

## [Endpoints](https://github.com/amadeulee/construcao-software-sgr/blob/master/SGR%20-%20Endpoints.pdf)

## Estratégia de controle de versão

  -  Utilização do Git e GitHub para se fazer o versionamento do código
  -  A atuação dos membros do grupo se deu através de branchs paralelas, criadas a partir da branch principal (development), onde foram disponibilizadas novas features e correções de bugs
  -  Após o commit e o push das mudanças se é criado uma "pull request" para que seja avaliado posteriormente e após isso, se faça o merge dela com a branch principal (development)

## Artefatos extras complementares:

- [Especificação estrutural final e completa da API](https://github.com/amadeulee/construcao-software-sgr/blob/2bdf2315119c5dd97ec61db1a2e5d5abddd245c9/Projeto-API.pdf)
- [Repositório com o código executável da API](https://github.com/lucamartins/ufg-cs-sgr-core-api)
- [Relatório do resultado da aplicação de técnicas de teste e qualidade](https://github.com/amadeulee/construcao-software-sgr/blob/master/Course%20-%20Software%20Testing%20and%20Quality%20Assurance%20-%20Prof.%20Mohamad%20Kassab.pdf)
