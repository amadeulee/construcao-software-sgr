# Projeto 01 - Entrega versão revisada
## Entrega da versão revisada do projeto


## Diagrama de classe: 
![image](https://github.com/amadeulee/construcao-software-sgr/assets/62031286/a48a3f12-4fb3-4e3f-a99f-d7cdb2374a20)

* PedidoStatus:
  * Status do pedido do cliente, pendente, em preparo, pronto e entregue

* Pedido:
  * Classe que diz respeito ao pedido propriamente dito, ele tem uma lista de pedidos com todos os itens solicitados, o status do pedido e a mesa que pediu

* Mesa:
  * Classe que possuí somente o id da mesa (o código de identificação dela) e um booleano dizendo se ela está livre ou ocupada

* ItemPedido:
  *  Classe referente ao Item do pedido do cliente. Ex: 1-Guaraná; 2-Coxinha. Possuí o atributo Item (referente ao item propriamente dito) e o atributo quantidade (quantas coxinhas o cliente pediu, por exemplo)

* Item:
  * Classe que refere ao item solicitado pelo cliente. Ex: X-bacon. Possuí o nome, o preço do pedido e uma lista com todos os ingredientes necessários para preparar o item.

* ItemIngrediente:
  * Classe que contém o nome do ingrediente e a quantidade (em gramas para comida e em quantidade para bebidas)

* Funcionario:
  * Classe que possuí os dados do funcionário (seja garçom, seja estoquista)

* Estoque:
  * Classe que possuí uma lista com todos os ingredientes existentes em estoque, cada item possuí um nome e a quantidade (atributos da classe estoqueIngrediente)

* estoqueIngrediente:
  * Classe que possuí o nome do ingrediente e a quantidade existente em estoque
