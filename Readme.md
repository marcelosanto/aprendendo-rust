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


# Tipos de Inteiros

<p>O u significa unsigned, enquanto o i significa signed, e o número que o segue é o número de bits. Por exemplo, um número do tipo u8 pode estar entre 0 e 255. E um numero do tipo i16 podem estar entre -32768  e 32767. As variantes de tamanho são os tipos inteiros de tamanho de ponteiro: usize e isize que são de 64 bits em uma CPU de 64 bits. O tipo de número inteiro padrão é i32, que significa que este tipo será usado pela inferência de tipo quando não puder escolher um tipo mais específico.</p>

# Tipos de Pontos Flutuantes

<p>Existem dois tipos de ponto flutuante: f32 e f64, sendo o último o padrão. O número após f representa o número de bits do tipo. Um exemplo de valor para ponto flutuante de exemplo é 0,31415e1.</p>