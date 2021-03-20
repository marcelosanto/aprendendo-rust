# Função Main

## Função principal

fn main () {
    println!("Hello, world!");
}

<p>Ele contém apenas uma função principal "main" - é onde a execução do programa começa. É uma função que não aceita argumentos (daí os parênteses vazios) e retorna um valor do tipo Unit, também escrita (). O corpo da função, entre colchetes, contém uma chamada para a macro println! () - podemos ver que esta é uma macro porque termina com !, em oposição a uma função. Esta macro imprime o texto entre parênteses, seguido por uma nova linha</p>


# Variáveis

Agora vamos mudar o programa anterior para adicionar uma variável:

fn main() {

let name = "world";

println!("Hello, {}!", name);

}

Aqui, vemos a inferência de tipo em ação - não temos que especificar o tipo da variável de nome pois o compilador irá inferir para nós. Poderíamos de modo facultativo explicitar o tipo como abaixo:

let name: &str = "world";

A partir de agora, vamos escrever todo código dentro da função principal main. No Rust, as variáveis são imutáveis por padrão. Como tal, escrever o seguinte causará um erro de compilação:

let age = 42;

age += 1;

O compilador nos dá uma mensagem de erro muito útil:

Para tornar uma variável mutável, precisamos usar a palavra-chave mut:

let mut age = 42;

age += 1;