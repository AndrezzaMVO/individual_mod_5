const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let propriedades = [];

console.log("Digite os comandos desejados do CSS (Quando encerrar, digite 'SAIR' para exibir a listagem):");

rl.on('line', (input) => {
    if (input === 'SAIR' || input === 'sair') {
        console.log(`Lista de propriedades CSS em ordem alfabética: ${propriedades.sort().join(', ')}`);
        rl.close();
    } else {
        propriedades.push(input);
    }
});
