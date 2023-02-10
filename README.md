# Desafio Dev Incrivel - HTML, CSS e JS
Desafio criado por mim para os alunos do bootcamp de desenvolvimento full stack da Tera. A ideia é apresentar um front end básico para os alunos melhorarem e implementarem os requisitos abaixo.

### Instruções
Você deverá criar a lógida da calculadora de simulação de crédito implementada neste projeto.

A interface está previamente definida, assim como os estilos.
Os desafios incluem refatorar o código e implementar funcionalidades (detalhados mais abaixo).

O que acha de encarar o desafio?


### Funcionalidade esperada

A aplicação deverá permitir ao usuário escolher o tipo de garantia que quer utilizar no pedido de empréstimo: ***"Veículo"*** ou ***"Imóvel"*** (o preenchimento padrão é *"Veículo"*) e seguir as regras de cálculo abaixo.

**Regras em comum**
- Taxa de IOF: 6.38%;
- Taxa de Juros: 2.34%;
- Valor máximo para empréstimo: 80% do valor da garantia;

*Fórmula do valor total a pagar*

```javascript
const valorTotalAPagar = ((iof / 100) + (taxaDeJuros / 100) + (prazo / 1000) + 1) * valorDoEmprestimo
```

*Fórmula do valor da parcela*

```javascript
const valorDaParcela = valorTotalAPagar / prazo
```

Ao mudar o tipo de garantia no elemento `select`, o usuário deve ver as opções de valores e prazos referentes ao tipo selecionado. Ou seja, ao selecionar veículo ou imóvel, você deve mostrar na tela opções diferentes nos campos do formulário para 'PRAZO' e validar valor mínimo e máximo de emprestimo e garantia usando Javascript. Veja abaixo os valores correspondentes:

**Veículo**
- Valor mínimo para empréstimo: R$ 3.000,00;
- Valor máximo para empréstimo: R$ 100.000,00;
- Prazos para veículo : 24 / 36 / 48 meses;
- Valor mínimo da garantia: R$ 5.000,00;
- Valor máximo da garantia: R$ 3.000.000,00; 

**Imóvel**
- Valor mínimo para empréstimo: R$ 30.000,00;
- Valor máximo para empréstimo: R$ 4.500.000,00;
- Prazos para imóvel : 120 / 180 / 240 meses;
- Valor mínimo da garantia: R$ 50.000,00;
- Valor máximo da garantia: R$ 100.000.000,00;

Por fim, ao clicar no botão 'Solicitar' você deve exibir os valores calculados nos campos: 'Valor da Parcela', 'Total a pagar', 'Taxa de juros'

<hr>
<h5> Desafio baseado no <a href="https://github.com/Creditas/challenge/tree/master/frontend"> tech challenge da Creditas </a> </h5>
