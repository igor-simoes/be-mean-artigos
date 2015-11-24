#Artigo

autor: Igor Simões - igorsimoes

Neste artigo irei abordar alguns conceitos da linguagem de programação Javascript e, através de exemplos, suas aplicações e alguma coisa a mais kkkk.

##Hoisting
```
Hoisting(em português, elevação) é o nome dado a um comportamento da linguagem de programação Javascript em que todas as declarações(variáveis ou funções) são direcionadas para o início do escopo* atual [1], ou seja, o compilador eleva todas as declarações para o topo do escopo e todas as execuções vão para o final do escopo de acordo com a ordem em que foi escrito. Ainda não entendeu? Vamos ao exemplo:
```
```Javascript
//exemplo 1 com variável
// saida : undefined Igor
try{
    console.log(nome);
    var nome = "Igor";
    console.log(nome);
}catch(e){
    console.log("erro!");
}
```
```
No exemplo 1, ao inicializar o script, a declaração da variável vai para o topo do escopo (apenas a declaração da variável nome e não sua inicialização). Por isso, ao entrar no bloco try, é mostrado no console que o valor da variável nome é undefined (ou seja, ela existe porém não foi inicializada). Na próxima linha, a variável é inicializada dentro do bloco try e é mostrado no console o valor desta variável, que neste caso é a string "Igor".
```
```Javascript
//exemplo 2 com função
// saida : "Hello World"
function helloWorld(){
    return msg;
    function msg(){
        return "Hello World";
    }
}
var hoisting = helloWorld();
hoisting();
```
```
No exemplo 2, se não houvesse o hoisting ocasionaria em undefined, mas o que ocorre ao executar a função helloWorld é o retorno da função msg(), que neste caso é o "hello world". Isto ocorre devido ao hoisting que segue uma ordem do escopo:

1. Declarações de variáveis (var hoisting = helloWorld();)
2. Declarações de funções (function msg(){ return "Hello World;}"})
3. Execuções (return msg;)
```



##Closure
```
Explique o que é, o porquê acontece e como usar. Cite situações que você usaria.
```
##Variável Global
```
Explique como se usa uma var Global dentro de uma função.
```
##Variável por parâmetro
```
Explique o que acontece dentro da função qnd um parâmetro é passado e também explique quando uma GLOBAL é passada por parâmetro.
```
##Instanciação usando uma IIFE
```
Explique como uma variável pode receber um valor de uma IIFE. Explique como passar uma variável por parâmetro para a IIFE e acontece com ela dentro da função.
```

## Referências

[1] http://wenndersantos.net/2014/12/javascript-hoisting/
