# CalculadoraDeImposto
Uma calculadora de imposto que usa funções Closure, Alta Ordem, List comprehensio e Lambda.

*Projeto: Cálculo de Imposto com Projeção Financeira*

Este documento descreve os requisitos relacionados à utilização de *Programação Funcional* no projeto, indicando onde cada conceito está implementado no código-fonte.

---

## ✅ Requisitos Funcionais e Implementação

### 1. Utilização de Função Lambda
O projeto utiliza uma função lambda (arrow function) para realizar o cálculo da projeção personalizada de rendimento mensal.

*Trecho do código:*
javascript
const calculoPersonalizado = (base, i) => base + (i + 1) * 10 + 100;

> Implementado dentro da função calculartaxa().

---

### 2. Utilização de List Comprehension (forma funcional)
Embora JavaScript não tenha sintaxe nativa de list comprehension, o conceito é aplicado com um for funcional dentro da função gerarProjecao():

*Trecho do código:*
javascript
for (let i = 0; i < meses.length; i++) {
    const novoValor = calculo(base, i);
    lista += `<li>${meses[i]}: R$ ${novoValor.toFixed(2)}</li>`;
}

> A função aplica um cálculo a cada item da lista meses, gerando uma projeção dinâmica.

---

### 3. Utilização de Closure
O projeto usa uma closure para criar uma função que preserva o valor de um bônus fixo.

*Trecho do código:*
javascript
function criarSomador(valorFixo) {
    return function (base) {
        return base + valorFixo;
    }
}

> A função somar100 é criada a partir de criarSomador(100), mantendo o valor 100 em seu escopo.

---

### 4. Utilização de Função de Alta Ordem
A função gerarProjecao() recebe uma função como argumento e a aplica sobre os dados, caracterizando uma função de alta ordem.

*Trecho do código:*
javascript
function gerarProjecao(base, meses, calculo) {
    // ...
    const novoValor = calculo(base, i);
    // ...
}

> A função calculo é passada como parâmetro e define a lógica da projeção.

---

## ✅ Conclusão

Todos os conceitos exigidos de *Programação Funcional* foram implementados e mapeados:

- [x] Função Lambda  
- [x] List Comprehension (forma funcional)  
- [x] Closure  
- [x] Função de Alta Ordem  

O projeto demonstra, de forma prática e funcional, o uso de técnicas modernas de programação em JavaScript.

## ✅ Integrantes


- [x] Gabriel Barboza Lima – 2315413 
- [x] Hiago Sampaio Lacerda de Moraes – 2319002
- [x] Isaque Freitas Melo – 2319000  
- [x] João Victor Queiroz Pacheco – 2314706
- [x] Natanael Barboza Lima – 2319722

O projeto demonstra, de forma prática e funcional, o uso de técnicas modernas de programação em JavaScript.
