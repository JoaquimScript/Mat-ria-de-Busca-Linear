//Exemplo de busca linear
function buscaLinear(arr, alvo) {
    for (let i = 0; i < arr.length; i++) {
        //Verificar se o elemento atual é o alvo
        if (arr[i] === alvo) {
            return i; //Retorna o índice
        }
    }
    return -1; //Retorna -1 se não encontrado
}

const lista = [10, 50, 30, 70, 80, 20];
console.log(buscaLinear(lista, 30)); //Saída: 2
console.log(buscaLinear(lista, 99)); //Saída: -1

function buscaLinear(arr, alvo) {
let inicio = 0;
let fim = arr.length - 1;

while (inicio <= fim) {
    let meio = Math.floor((inicio + fim) / 2);

    if (arr[meio] === alvo) {
        return meio; // Retorna o índice do elemento encontrado
    } else if (arr[meio] < alvo) {
        inicio = meio + 1; // Continua a busca na metade direita
    } else {
        fim = meio - 1; // Continua a busca na metade esquerda
    }
    return -1; // Retorna -1 se o elemento não for encontrado
}

const numeros = [2, 5, 8, 12, 16, 23, 38, 56, 72, 91];}
console.log(buscaLinear(numeros, 23)); // Saída: 5


function gerarListaAleatoria(tamanho) {
 
    const lista = []
 
    for (let i = 0; i < tamanho; i++) {
 
        // números aleatórios entre 1 e 2000
        lista.push(Math.floor(Math.random() * 2000) + 1)
    }
 
    return lista
}
 
function buscaLinear(lista, valor) {
 
    for (let i = 0; i < lista.length; i++) {
 
        // mostra o número sendo analisado
        console.log("Verificando:", lista[i])
 
        if (lista[i] === valor) {
            return i
        }
    }
 
    return -1
}
 
// ===============================
// GERA LISTA
// ===============================
 
let numeros = gerarListaAleatoria(2000)
 
// Número procurado
let valorProcurado = 1500
 
console.log("Número procurado:", valorProcurado)
 
// ===============================
// EXECUTA BUSCA
// ===============================
 
let resultado = buscaLinear(numeros, valorProcurado)
 
// ===============================
// RESULTADO
// ===============================
 
if (resultado !== -1) {
 
    console.log(
        `Valor encontrado na posição ${resultado}`
    )
 
} else {
 
    console.log("Valor não encontrado")
}
