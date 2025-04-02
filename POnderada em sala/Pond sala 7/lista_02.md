Lista de Exercícios 02

Questões Objetivas

 1) Alternativa correta:
A) O código avalia a expressão booleana, imprime true, calcula o produto dos números na lista e imprime o resultado no console.

 2) Alternativa correta:
B) analisarCredito1() exibirá: 'Seu crédito foi negado. Saldo disponível: -600.', enquanto analisarCredito2() exibirá: 'Seu crédito foi negado. Saldo disponível: -200.'

 3) Alternativa correta:
D) O código verifica se a idade é menor de 18, entre 18 e 60 ou acima de 60, imprimindo uma mensagem específica para cada caso.

 4) Alternativa correta:
 B) Dispositivo 1 ligado. Energia restante: 900 
 Dispositivo 2 ligado com bateria extra. Energia restante: 700 
 Dispositivo 3 ligado. Energia restante: 200  
 Dispositivo 4 não pode ser ligado. Energia insuficiente.
 Dispositivo 5 não pode ser ligado. Energia insuficiente.

 5) Alternativa correta:
 B) O método update() é chamado continuamente a cada quadro (frame) do jogo, sendo usado para atualizar a lógica, movimentação e interações dos objetos na cena.

 6) Alternativa correta:
 A) Simular física avançada, incluindo corpos rígidos, colisões complexas e interação entre objetos com gravidade e forças.

---

Questões Dissertativas

 7) Pseudocódigo - Classificação do frete
```javascript
function calcularFrete(valorCompra) {
    if (valorCompra < 50) {
        console.log("Frete não disponível!");
    } else if (valorCompra <= 199.99) {
        console.log("Frete com custo adicional!");
    } else {
        console.log("Frete grátis!");
    }
}
```

---

8) Pseudocódigo - Classe `Veiculo`, `Carro` e `Moto`
```javascript
class Veiculo {
    constructor(modelo, ano) {
        this.modelo = modelo;
        this.ano = ano;
    }

    calcularConsumo() {
        console.log("O consumo será calculado na subclasse.");
    }
}

class Carro extends Veiculo {
    constructor(modelo, ano, consumoPorKm) {
        super(modelo, ano);
        this.consumoPorKm = consumoPorKm;
    }

    calcularConsumo(distancia) {
        return distancia / this.consumoPorKm;
    }
}

class Moto extends Veiculo {
    constructor(modelo, ano, consumoPorKm) {
        super(modelo, ano);
        this.consumoPorKm = consumoPorKm;
    }

    calcularConsumo(distancia) {
        return distancia / this.consumoPorKm;
    }
}
```

---

9) Pseudocódigo - Cálculo de tempo para pouso seguro
```javascript
function calcularPouso(velocidadeInicial, desaceleracao, tempoMaximo, velocidadeSegura) {
    let tempo = 0;
    let velocidade = velocidadeInicial;

    while (velocidade > velocidadeSegura && tempo < tempoMaximo) {
        velocidade -= desaceleracao;
        tempo++;
    }

    if (velocidade <= velocidadeSegura) {
        console.log(`A sonda atingiu uma velocidade segura em ${tempo} segundos.`);
    } else {
        console.log("A sonda não conseguiu reduzir a tempo.");
    }
}
```

---

 10) Pseudocódigo - Multiplicação de Matrizes de Investimento
```javascript
function multiplicarMatrizes(A, B) {
    if (A[0].length !== B.length) {
        return "As matrizes não podem ser multiplicadas. Dimensões incompatíveis.";
    }

    let resultado = [];
    for (let i = 0; i < A.length; i++) {
        resultado[i] = [];
        for (let j = 0; j < B[0].length; j++) {
            let soma = 0;
            for (let k = 0; k < A[0].length; k++) {
                soma += A[i][k] * B[k][j];
            }
            resultado[i][j] = soma;
        }
    }
    return resultado;
}

let investimentosAno1 = [[1000, 2000], [1500, 2500]];
let investimentosAno2 = [[1200, 1800], [1300, 2700]];
let resultadoInvestimento = multiplicarMatrizes(investimentosAno1, investimentosAno2);
console.log("Resultado da multiplicação das matrizes de investimento:", resultadoInvestimento);
