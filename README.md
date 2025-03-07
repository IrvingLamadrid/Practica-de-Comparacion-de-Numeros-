# Practica-de-Comparacion-de-Numeros-
Comparar los número 2, 4
// obtener los números del usuario
function obtener Num() {
    let num1 = parseInt(prompt("Introduce el primer número"));
    let num2 = parseInt(prompt("Introduce el segundo número"));
    let num3 = parseInt(prompt("Ingrese el tercer número"));

    return [num1, num2, num3];
}

// Función para ordenar los números
function ordenarNumeros(numeros) {
    // Orden ascendente
    let ascendente = numeros.slice().sort((a, b) => a - b);
    
    // Orden descendente
    let descendente = numeros.slice().sort((a, b) => b - a);

    return { ascendente, descendente };
}

// Función para verificar si los números son iguales
function verificarIguales(numeros) {
    return new Set(numeros).size === 1;
}

// Función principal
function main() {
    let numeros = obtenerNumeros();
    let { ascendente, descendente } = ordenarNumeros(numeros);

    console.log("Números en orden descendente:", descendente.join(', '));
    console.log("Números en orden ascendente:", ascendente.join(', '));

    if (verificarIguales(numeros)) {
        console.log("Todos los números son iguales.");
    }
}

main();

