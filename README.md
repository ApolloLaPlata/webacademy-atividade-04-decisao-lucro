# Atividade 4 — Estruturas de Controle e Decisão em Algoritmos

**Curso:** Web Academy UFAC  
**Disciplina:** Algoritmos e Lógica de Programação  
**Aluno:** Vinicius Miranda de Farias

## Enunciado

Na loja do Seu Marcos, a margem de lucro depende do valor de compra:

- valor de compra **menor que R$ 10,00** → lucro de **30%**;
- valor de compra **igual ou maior que R$ 10,00** → lucro de **20%**.

O algoritmo deve ler o valor de compra, aplicar `se / senao`, calcular o lucro e o preço final de venda e mostrar ambos com **2 casas decimais**, usando a biblioteca `Matematica` do Portugol Studio.

## Algoritmo completo em Portugol Studio

```
programa {
    inclua biblioteca Matematica --> m
    funcao inicio() {
        real valorCompra, taxa, lucro, precoFinal
        escreva("Digite o valor de compra do produto: ")
        leia(valorCompra)

        se (valorCompra < 10) {
            taxa = 0.30
        } senao {
            taxa = 0.20
        }

        lucro = valorCompra * taxa
        precoFinal = valorCompra + lucro

        escreva("Lucro: R$ ", m.arredondar(lucro, 2))
        escreva("Preco final de venda: R$ ", m.arredondar(precoFinal, 2))
    }
}
```

## Resposta por etapa

### 1. Leitura do valor de compra

```
real valorCompra
escreva("Digite o valor de compra do produto: ")
leia(valorCompra)
```

A variável `valorCompra` é do tipo `real` porque o preço pode ter casas decimais.

### 2. Decisão com `se / senao`

```
real taxa
se (valorCompra < 10) {
    taxa = 0.30
} senao {
    taxa = 0.20
}
```

Se o valor for menor que 10, usa-se 30%; caso contrário (igual ou maior que 10), usa-se 20%.

### 3. Cálculo do lucro e do preço final

```
real lucro, precoFinal
lucro = valorCompra * taxa
precoFinal = valorCompra + lucro
```

O lucro é o valor de compra multiplicado pela taxa; o preço final é o valor de compra somado ao lucro.

### 4. Saída com arredondamento para 2 casas decimais

```
inclua biblioteca Matematica --> m
...
escreva("Lucro: R$ ", m.arredondar(lucro, 2))
escreva("Preco final de venda: R$ ", m.arredondar(precoFinal, 2))
```

A biblioteca `Matematica` é incluída antes de `funcao inicio()`, e a função `m.arredondar(valor, 2)` ajusta ambos os valores para duas casas decimais, conforme o exemplo da Aula 4.
