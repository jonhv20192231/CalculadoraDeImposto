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

*Ilustração*

![Foto 1 copiar](https://github.com/user-attachments/assets/51355013-d8da-4aca-b381-c25a1d1162eb)



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


*Ilustração*

![Foto 2 copiar](https://github.com/user-attachments/assets/2a745676-c5cd-42c9-997b-0ae45a47157e)


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

*Ilustração*

![Foto 3 copiar](https://github.com/user-attachments/assets/773ec03d-7fde-4877-abaa-35f8d925ba10)


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


*Ilustração*

![Foto 4 copiar](https://github.com/user-attachments/assets/1a5578dc-c3ea-445f-9b84-621fc08f78c2)

---
### 5. Requisitos Funcionais
- [x] O sistema permite que o usuário calcule o seu faturamento e a taxa, dando o resultado líquido 
do valor.  
- [x] Ao clicar em calcular, o sistema irá efetuar o cálculo e a partir do resultado irá projetar quanto 
irá gerar dentro de 10 meses.  
- [x] Quando o usuário depositar o valor, a página emitirá um alerta agradecendo pela confiança e 
em seguida irá atualizar. 
- [x] O sistema mostrará o valor calculado e irá criar a projeção de quanto irá gerar ao depositar esse 
dinheiro. 
- [x] O sistema irá oferecer um desconto de 100 reais no primeiro deposito ao depositar pela 
primeira vez. 
- [x] O sistema alertará que você recebeu um bônus de 100 reais pelo valor depositado

---
### 5. Requisitos Não Funcionais
- [x] O sistema irá calcular e projetar o valor que o usuário colocou rapidamente. 
- [x] O sistema está disponível apenas para computador 
- [x] O layout é responsivo, simples e objetivo no que se propõe  
- [x] O fundo da página tem uma cor confortável para os olhos 
- [x] O botão mudará de cor ao passar o mouse  
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

---
## ✅ Papel de cada um dos Integrantes envolvido no projeto 
- [x] Gabriel Barboza Lima – Teste do código 
- [x] Hiago Sampaio Lacerda de Moraes – Documentação dos Requisitos 
- [x] Isaque Freitas Melo – Documentação dos Requisitos 
- [x] João Victor Queiroz Pacheco – Implementação do código 
- [x] Natanael Barboza Lima – Implementação do código 

## Fonte de pesquisa e Auxílio
---

 - **Chatgpt**
   - Objetivo: Auxilio na estruturação e Correção de Bugs
   - Url: https://chatgpt.com/share/67ddb2ee-7ad8-8013-b5ea-41ce7523358f
    https://chatgpt.com/share/67ddb2fd-270c-8013-b75e-2c6cd988d5fb
    0bs: Talvez o chat fique indisponível devido ao tempo que ele determina, pensando nisso, está presente também nos arquivos, uma parte em vídeo mostrando o auxíio que ele ofereceu.
