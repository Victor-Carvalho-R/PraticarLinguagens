# 🚀 Desafios de Programação

Repositório para aprender linguagens de programação na prática. Aqui estão **304 desafios** que vão do "Olá, Mundo" até mini projetos, com foco em **lógica** (e não em decorar fórmulas). Cada pessoa escolhe uma linguagem (ex.: C, Java, Python, Rust, Go, JavaScript...) e resolve os mesmos desafios na sua própria linguagem. Depois, é só comparar as soluções! 🙂

> 🧩 Este arquivo é **neutro em relação à linguagem**. Para treinar recursos específicos de C, Python, JavaScript, Java, C#, TypeScript e Rust, veja o [`DESAFIOS_POR_LINGUAGEM.md`](DESAFIOS_POR_LINGUAGEM.md).

## 📖 Como usar

1. Escolha sua linguagem e crie uma pasta com o nome dela (ex.: `python/`, `rust/`, `csharp/`).
2. Resolva os desafios **em ordem** (ou pule os que quiser, mas as seções vão ficando mais difíceis).
3. Salve cada solução com o número do desafio no nome do arquivo (ex.: `python/001.py`, `rust/001.rs`).
4. Ao terminar, marque ✅ na coluna da sua pessoa na tabela.
5. Faça *commits* pequenos, um por desafio, com mensagens como `desafio 042: ano bissexto`.
6. Revisem o código um do outro via *Pull Request* e comparem as diferenças entre as linguagens. É aí que se aprende mais!

> 💡 Edite o cabeçalho das tabelas trocando **Dev 1** e **Dev 2** pelos nomes de vocês (e adicione mais colunas se entrar mais gente).

## 📁 Estrutura sugerida

```
.
├── DESAFIOS.md
├── DESAFIOS_POR_LINGUAGEM.md
├── <linguagem-do-dev-1>/
│   ├── 001.<ext>
│   ├── 002.<ext>
│   └── ...
└── <linguagem-do-dev-2>/
    ├── 001.<ext>
    ├── 002.<ext>
    └── ...
```

## 📏 Regras de ouro

- **Nada de copiar e colar** de IA ou da internet. Pode pesquisar a sintaxe, mas a lógica é sua.
- Os enunciados são propositalmente abertos: **invente seus próprios casos de teste**, principalmente os casos de borda (zero, negativo, vazio, tudo igual...).
- Se travar, peça uma dica ao colega antes de olhar uma solução pronta.
- Em desafios com "sem função pronta", implemente na mão. O objetivo é aprender como funciona por dentro.
- Trate entradas inválidas quando fizer sentido (divisão por zero, número negativo, texto vazio...).
- Se um desafio não fizer sentido na sua linguagem, pule e anote o motivo.
- **Bônus:** refaça um desafio antigo de outro jeito (outra estrutura, recursão x laço, mais eficiente).

## 🗂️ Índice

- [🟢 1. Fundamentos](#-1-fundamentos) — desafios 001 a 017
- [🟢 2. Condicionais](#-2-condicionais) — desafios 018 a 040
- [🟡 3. Laços de repetição](#-3-laços-de-repetição) — desafios 041 a 074
- [🟡 4. Strings](#-4-strings) — desafios 075 a 116
- [🟡 5. Arrays e matrizes](#-5-arrays-e-matrizes) — desafios 117 a 153
- [🟠 6. Funções e recursão](#-6-funções-e-recursão) — desafios 154 a 180
- [🟠 7. Ordenação, busca e algoritmos clássicos](#-7-ordenação-busca-e-algoritmos-clássicos) — desafios 181 a 202
- [🔴 8. Estruturas de dados (faça você mesmo, sem bibliotecas prontas)](#-8-estruturas-de-dados-faça-você-mesmo-sem-bibliotecas-prontas) — desafios 203 a 228
- [🔴 9. Arquivos e entrada/saída](#-9-arquivos-e-entradasaída) — desafios 229 a 248
- [🔴 10. Structs, classes e orientação a objetos](#-10-structs-classes-e-orientação-a-objetos) — desafios 249 a 265
- [⚫ 11. Mini projetos](#-11-mini-projetos) — desafios 266 a 304

## 🟢 1. Fundamentos

| # | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| 001 | Imprimir "Olá, Mundo!", depois perguntar o nome do usuário e responder "Olá, <nome>!" | | |
| 002 | Ler dois números e mostrar soma, subtração, multiplicação, divisão e resto (cuidado com divisão por zero) | | |
| 003 | Ler uma linha com dois números separados por espaço (ex.: `12 7`) e mostrar a soma | | |
| 004 | Entender divisão inteira vs. divisão real: mostrar `7 / 2` das duas formas e explicar a diferença | | |
| 005 | Ler três notas e calcular a média | | |
| 006 | Ler um valor em segundos e mostrar no formato `HH:MM:SS` (com zeros à esquerda) | | |
| 007 | Ler um horário de início (hora e minuto) e uma duração em minutos e mostrar o horário de término (ex.: 23:50 + 30 min = 00:20) | | |
| 008 | Trocar o valor de duas variáveis, com e sem variável auxiliar | | |
| 009 | Rotacionar o valor de três variáveis (a → b → c → a) | | |
| 010 | Dado um valor em reais, mostrar a quantidade mínima de notas (100, 50, 20, 10, 5, 2) e moedas de 1 para pagá-lo | | |
| 011 | Dividir uma conta entre N pessoas; se a divisão não for exata, mostrar quanto cada um paga e quantos pagam 1 centavo a mais | | |
| 012 | Ler um número de 3 dígitos e mostrar centena, dezena e unidade separadamente (sem converter para texto) | | |
| 013 | Mostrar o código ASCII de um caractere lido e o caractere correspondente a um código lido | | |
| 014 | Mostrar o menor e o maior valor que cada tipo numérico da sua linguagem consegue guardar (se houver limite) | | |
| 015 | Descobrir o que acontece quando um inteiro passa do limite na sua linguagem (estoura, dá a volta, vira número grande?) e explicar | | |
| 016 | Mostrar AND, OR, XOR, NOT e deslocamentos (`<<`, `>>`) entre dois números lidos, em decimal e em binário | | |
| 017 | Imprimir um número real com 2 casas decimais, alinhado à direita em 10 colunas e com zeros à esquerda | | |

## 🟢 2. Condicionais

| # | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| 018 | Dado um número, dizer se é positivo, negativo ou zero, e também se é par ou ímpar | | |
| 019 | Ler três números e mostrar o maior (sem array e sem função pronta) | | |
| 020 | Ler três números e mostrá-los em ordem crescente (sem array e sem `sort`) | | |
| 021 | Aluno aprovado: nota >= 7 e frequência >= 75%. Recuperação: nota entre 5 e 7 com frequência ok. Caso contrário, reprovado. Mostrar o resultado e o motivo | | |
| 022 | Ler a nota de 3 jurados, descartar a maior e a menor e mostrar a que sobrou | | |
| 023 | Verificar se um ano é bissexto | | |
| 024 | Ler mês e ano e mostrar quantos dias o mês tem | | |
| 025 | Validar uma data completa (dia, mês, ano) | | |
| 026 | Dadas duas datas (dia, mês, ano), dizer qual vem primeiro ou se são iguais | | |
| 027 | Dado dia e mês de nascimento e a data de hoje, dizer se a pessoa já fez aniversário este ano | | |
| 028 | Ler um número de 1 a 7 e imprimir o dia da semana (use `switch`/`match`) | | |
| 029 | Ler dois números e um operador (+, -, *, /, %) e mostrar o resultado, tratando divisão por zero e operador inválido | | |
| 030 | Classificar um caractere: vogal, consoante, dígito, espaço ou símbolo | | |
| 031 | Verificar se três lados formam um triângulo e classificá-lo (equilátero, isósceles, escaleno) | | |
| 032 | Dado o dia da semana e o horário, dizer se a loja está aberta (seg a sex 9h–18h, sáb 9h–13h, dom fechado) | | |
| 033 | Ingresso de cinema: crianças até 12 anos e idosos 60+ pagam meia; estudante paga meia; descontos não se acumulam; às quartas todos pagam meia. Calcule o preço | | |
| 034 | Aprovar ou negar uma compra no cartão: limite disponível, cartão bloqueado ou não, e compras acima de R$ 1.000 exigem senha. Mostrar o motivo da negativa | | |
| 035 | Pedra, papel e tesoura: dois jogadores digitam a jogada e o programa diz quem venceu | | |
| 036 | Dado um ponto (x, y), dizer em qual quadrante está ou se está em algum eixo | | |
| 037 | Dados dois intervalos [a, b] e [c, d], dizer se eles se sobrepõem e qual é a sobreposição | | |
| 038 | Dada uma casa de xadrez (ex.: `e4`), dizer se ela é branca ou preta | | |
| 039 | Dadas duas casas de xadrez, dizer se um cavalo consegue ir de uma para a outra em um movimento | | |
| 040 | Dadas duas casas de xadrez, dizer se uma torre e se um bispo conseguem ir de uma para a outra em um movimento (sem peças no caminho) | | |

## 🟡 3. Laços de repetição

| # | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| 041 | Imprimir de 1 até N e depois de N até 1 | | |
| 042 | Imprimir os múltiplos de K entre A e B e mostrar quantos são e a soma deles | | |
| 043 | Imprimir a tabuada de um número; depois, a tabuada de 1 a 10 em colunas alinhadas | | |
| 044 | Calcular o fatorial de N | | |
| 045 | Calcular A elevado a B (B inteiro >= 0) sem usar função de potência | | |
| 046 | Ler números até o usuário digitar 0 e mostrar quantidade, soma, média, maior e menor | | |
| 047 | Dado um número, mostrar quantos dígitos tem, a soma deles e o maior dígito | | |
| 048 | Inverter um número (123 → 321) | | |
| 049 | Verificar se um número é palíndromo (sem converter para texto) | | |
| 050 | Imprimir os N primeiros termos da sequência de Fibonacci | | |
| 051 | Listar todos os números primos até N | | |
| 052 | Calcular o MDC de dois números (algoritmo de Euclides) | | |
| 053 | Decompor um número em fatores primos (60 → 2 × 2 × 3 × 5) | | |
| 054 | Converter um número decimal para qualquer base de 2 a 16 | | |
| 055 | Converter um número escrito em qualquer base de 2 a 16 para decimal | | |
| 056 | Imprimir um triângulo de asteriscos com N linhas | | |
| 057 | Imprimir uma pirâmide centralizada de asteriscos | | |
| 058 | Imprimir um losango oco | | |
| 059 | Imprimir o triângulo de Pascal | | |
| 060 | FizzBuzz: de 1 a 100, imprimir Fizz para múltiplos de 3, Buzz para múltiplos de 5 e FizzBuzz para ambos | | |
| 061 | Jogo de adivinhação: o programa sorteia de 1 a 100 e o jogador tem 7 tentativas, recebendo dicas de "maior" ou "menor" | | |
| 062 | Adivinhação invertida: você pensa em um número de 1 a 100 e o computador tenta adivinhar (você responde "maior", "menor" ou "acertou"). Ele deve acertar em no máximo 7 tentativas | | |
| 063 | Menu repetitivo (1 - Somar, 2 - Subtrair, 0 - Sair) que roda até o usuário escolher sair | | |
| 064 | Pedir uma senha com no máximo 3 tentativas e bloquear em seguida | | |
| 065 | Imprimir todas as horas de um dia (00:00 a 23:59) que são palíndromas (ex.: 12:21) | | |
| 066 | Contar quantas vezes o dígito 7 aparece em todos os números de 1 a 1000 | | |
| 067 | Quantos números de 1 a 10.000 são palíndromos? | | |
| 068 | Jogar um dado até sair 6 e contar as tentativas; repetir 1000 vezes e calcular a média | | |
| 069 | Jogo de Nim: 21 palitos, cada jogador retira de 1 a 3, quem pegar o último perde. Jogue contra o computador (descubra a estratégia vencedora) | | |
| 070 | Problema de Josephus: N pessoas em círculo, eliminando uma a cada K; quem sobra? | | |
| 071 | Fila de banco: dados os tempos de atendimento de N clientes e 2 caixas, simular para qual caixa cada cliente vai e mostrar o tempo total | | |
| 072 | Quantos meses leva para juntar R$ 10.000 guardando R$ 300 por mês, com aumento de R$ 20 no depósito a cada 6 meses? | | |
| 073 | Sequência de Collatz: dado N, imprimir a sequência até 1 e o número de passos; depois, achar qual N até 10.000 gera a sequência mais longa | | |
| 074 | Imprimir uma tabela de multiplicação N × N com colunas alinhadas | | |

## 🟡 4. Strings

| # | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| 075 | Implementar `tamanho(s)` sem usar a função pronta | | |
| 076 | Inverter uma string | | |
| 077 | Verificar se uma frase é palíndromo, ignorando espaços, pontuação e maiúsculas | | |
| 078 | Contar vogais, consoantes, dígitos, espaços e símbolos de um texto | | |
| 079 | Contar as palavras de uma frase (cuidado com espaços repetidos) | | |
| 080 | Implementar `paraMaiusculas` e `paraMinusculas` sem função pronta | | |
| 081 | Capitalizar a primeira letra de cada palavra | | |
| 082 | Mostrar a frequência de cada letra de um texto, em ordem decrescente | | |
| 083 | Verificar se duas palavras são anagramas | | |
| 084 | Cifra de César: cifrar e decifrar com deslocamento K | | |
| 085 | Implementar `contem(texto, trecho)` e `indiceDe(texto, trecho)` sem função pronta | | |
| 086 | Implementar `substituir(texto, antigo, novo)` sem função pronta | | |
| 087 | Compressão RLE ("aaabbc" → "a3b2c1") | | |
| 088 | Descompressão RLE ("a3b2c1" → "aaabbc") | | |
| 089 | Encontrar o primeiro caractere que não se repete ("aabcc" → "b") | | |
| 090 | Verificar se todos os caracteres de uma string são únicos | | |
| 091 | Encontrar a maior substring sem caracteres repetidos ("abcabcbb" → "abc") | | |
| 092 | Verificar se uma string é rotação de outra ("abcde" e "cdeab") | | |
| 093 | Verificar se duas strings diferem em no máximo um caractere (inserção, remoção ou troca) | | |
| 094 | Verificar se parênteses, colchetes e chaves estão balanceados ("{[()]}" ok, "{[(])}" não) | | |
| 095 | Validar a força de uma senha: mínimo de 8 caracteres, maiúscula, minúscula, dígito e símbolo; mostrar o que está faltando | | |
| 096 | Validar um e-mail com regras simples (um `@`, texto antes e depois, ponto no domínio) | | |
| 097 | Validar um endereço IPv4 (4 números de 0 a 255 separados por ponto) | | |
| 098 | Mascarar dados: "joao@email.com" → "j***@email.com" e "1234567890" → "******7890" | | |
| 099 | Escrever um número de 0 a 999 por extenso | | |
| 100 | Converter número romano para decimal | | |
| 101 | Converter decimal (1 a 3999) para romano | | |
| 102 | Encontrar a palavra mais longa de uma frase | | |
| 103 | Inverter a ordem das palavras ("eu amo código" → "código amo eu") | | |
| 104 | Implementar `atoi` e `itoa` (string ↔ inteiro) sem função pronta | | |
| 105 | Implementar `comparar(a, b)` (retorna negativo, zero ou positivo) sem função pronta | | |
| 106 | Implementar `split(texto, separador)` e `join(lista, separador)` | | |
| 107 | Implementar `trim`: remover espaços do começo e do fim | | |
| 108 | Converter `snake_case` para `camelCase` e de volta | | |
| 109 | Encontrar a maior substring palíndroma de uma string | | |
| 110 | Encontrar o maior prefixo comum entre várias strings | | |
| 111 | Quebra de linha (word wrap): dado um texto e uma largura N, quebrar em linhas sem cortar palavras | | |
| 112 | Sequência look-and-say: 1, 11, 21, 1211, 111221... (cada termo descreve o anterior) | | |
| 113 | Converter horário de 24h para 12h ("17:45" → "5:45 PM") e de volta | | |
| 114 | Formatar um número com separador de milhar (1234567 → "1.234.567") | | |
| 115 | Desenhar um texto dentro de uma caixa, com bordas ajustadas à maior linha | | |
| 116 | Verificar se uma frase é pangrama (tem todas as letras do alfabeto) | | |

## 🟡 5. Arrays e matrizes

| # | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| 117 | Ler N números em um array e mostrar soma, média, maior e menor (com as posições) | | |
| 118 | Inverter um array (in-place) | | |
| 119 | Buscar um elemento e retornar todas as posições onde aparece (ou avisar que não existe) | | |
| 120 | Separar um array em dois: pares e ímpares, mantendo a ordem | | |
| 121 | Inserir um elemento em uma posição e remover um elemento de uma posição, deslocando os demais | | |
| 122 | Remover elementos duplicados mantendo a primeira ocorrência | | |
| 123 | Dados dois arrays, calcular união, interseção e diferença | | |
| 124 | Mesclar dois arrays já ordenados em um só (sem reordenar do zero) | | |
| 125 | Rotacionar um array K posições para a direita (in-place) | | |
| 126 | Encontrar o segundo maior valor distinto em uma única passada | | |
| 127 | Calcular a mediana | | |
| 128 | Encontrar a moda (valor mais frequente) | | |
| 129 | Verificar se um array está ordenado (crescente, decrescente ou nenhum dos dois) | | |
| 130 | Verificar se um array de tamanho N é uma permutação de 1 a N | | |
| 131 | Encontrar o número que falta em uma sequência de 1 a N | | |
| 132 | Encontrar o maior trecho crescente consecutivo | | |
| 133 | Subarray contíguo com a maior soma (Kadane) | | |
| 134 | Encontrar dois números do array que somam um alvo | | |
| 135 | Mover todos os zeros para o final mantendo a ordem dos outros | | |
| 136 | Encontrar o ponto de equilíbrio (índice onde a soma à esquerda = soma à direita) | | |
| 137 | Melhor dia para comprar e vender: dados os preços diários de uma ação, achar o maior lucro possível (comprar antes de vender) | | |
| 138 | Maior sequência de dias sem vendas em uma lista de vendas diárias | | |
| 139 | Ranking: dado um array de pontuações, mostrar a posição de cada jogador (empates dividem a mesma posição) | | |
| 140 | Agenda: dadas várias reuniões (início, fim), mesclar as que se sobrepõem | | |
| 141 | Transposta de uma matriz | | |
| 142 | Soma de cada linha, de cada coluna e das duas diagonais de uma matriz | | |
| 143 | Verificar se uma matriz é simétrica | | |
| 144 | Verificar se uma matriz é um quadrado mágico | | |
| 145 | Imprimir uma matriz em espiral | | |
| 146 | Rotacionar uma matriz 90° | | |
| 147 | Verificar o vencedor de um jogo da velha a partir de um tabuleiro 3×3 | | |
| 148 | Verificar se há 4 peças em linha em um tabuleiro de Connect 4 | | |
| 149 | Verificar se uma cartela de bingo 5×5 tem linha, coluna ou diagonal completa, dados os números sorteados | | |
| 150 | Validar um tabuleiro de Sudoku preenchido | | |
| 151 | Campo minado: dada a matriz de minas, calcular o número de cada célula | | |
| 152 | Jogo da Vida de Conway: calcular uma geração | | |
| 153 | Imprimir um histograma em texto a partir de um array de valores | | |

## 🟠 6. Funções e recursão

| # | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| 154 | Criar `maior(a, b, c)` e `ehPrimo(n)` e usá-las em um programa | | |
| 155 | Criar funções que recebem um array: média, maior valor e contagem de elementos que atendem a uma condição | | |
| 156 | Função que retorna mais de um valor (ex.: mínimo e máximo de um array) | | |
| 157 | Escrever uma função `trocar(a, b)` que troque os valores das variáveis de quem chamou. Funcionou? Se não, por quê? | | |
| 158 | Escopo: demonstrar variável global, local e de módulo/classe (ou o equivalente na sua linguagem) e o que cada uma enxerga | | |
| 159 | Passar uma função como argumento (ex.: aplicar uma operação a cada elemento de um array) | | |
| 160 | Função com número variável de argumentos (`soma(1, 2, 3, ...)`) | | |
| 161 | Fatorial recursivo | | |
| 162 | Fibonacci recursivo e depois com memoização (compare o tempo) | | |
| 163 | Inverter uma string e verificar palíndromo, ambos de forma recursiva | | |
| 164 | Somar, contar e achar o maior elemento de um array de forma recursiva | | |
| 165 | Torre de Hanói (imprimir os movimentos) | | |
| 166 | Gerar todas as permutações de uma string | | |
| 167 | Gerar todos os subconjuntos de um conjunto | | |
| 168 | Gerar todas as combinações de parênteses válidos com N pares | | |
| 169 | Gerar todas as senhas de tamanho N com um alfabeto dado | | |
| 170 | Contar os caminhos de um canto a outro de uma grade N × M, andando só para a direita e para baixo | | |
| 171 | De quantas formas se sobe uma escada de N degraus subindo 1 ou 2 de cada vez? | | |
| 172 | Troco: mínimo de moedas para um valor e de quantas formas diferentes é possível dar o troco (programação dinâmica) | | |
| 173 | Distância de edição (Levenshtein) entre duas palavras | | |
| 174 | Problema das N rainhas | | |
| 175 | Encontrar o caminho em um labirinto (matriz de 0 e 1) com backtracking | | |
| 176 | Flood fill: pintar uma região conexa de uma matriz | | |
| 177 | Contar "ilhas" (grupos conectados de 1s) em uma matriz de 0 e 1 | | |
| 178 | Resolver Sudoku por backtracking | | |
| 179 | Subset sum: dado um conjunto e um alvo, dizer se algum subconjunto soma o alvo | | |
| 180 | Problema dos jarros: com jarros de 3 L e 5 L, obter exatamente 4 L (busca de estados) | | |

## 🟠 7. Ordenação, busca e algoritmos clássicos

| # | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| 181 | Busca linear | | |
| 182 | Busca binária (iterativa) | | |
| 183 | Busca binária pela resposta: calcular a raiz quadrada inteira de N | | |
| 184 | Buscar um valor em um array ordenado que foi rotacionado (ex.: `[4, 5, 6, 1, 2, 3]`) | | |
| 185 | Bubble sort | | |
| 186 | Selection sort | | |
| 187 | Insertion sort | | |
| 188 | Merge sort | | |
| 189 | Quick sort | | |
| 190 | Counting sort | | |
| 191 | Ordenar um array de strings em ordem alfabética (sem função de sort pronta) | | |
| 192 | Ordenar pessoas por idade e, em caso de empate, por nome. Teste se a sua ordenação é estável | | |
| 193 | Comparar os algoritmos: contar comparações e medir o tempo com 10, 1.000 e 100.000 elementos | | |
| 194 | Encontrar o K-ésimo maior elemento sem ordenar tudo | | |
| 195 | Crivo de Eratóstenes | | |
| 196 | Embaralhar um array (Fisher-Yates) | | |
| 197 | Escolher o máximo de reuniões sem conflito de horário (algoritmo guloso) | | |
| 198 | Busca em largura (BFS): menor caminho em um labirinto | | |
| 199 | Busca em profundidade (DFS) em um grafo | | |
| 200 | Detectar ciclo em um grafo | | |
| 201 | Ordem de execução: dadas dependências entre tarefas, achar uma ordem válida (ordenação topológica) | | |
| 202 | Menor caminho entre cidades com distâncias (Dijkstra) | | |

## 🔴 8. Estruturas de dados (faça você mesmo, sem bibliotecas prontas)

| # | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| 203 | Pilha (stack) com array | | |
| 204 | Fila (queue) com array circular | | |
| 205 | Lista encadeada simples (inserir no início/fim, remover, buscar, imprimir) | | |
| 206 | Lista duplamente encadeada | | |
| 207 | Inverter uma lista encadeada | | |
| 208 | Detectar ciclo em uma lista encadeada | | |
| 209 | Encontrar o elemento do meio de uma lista encadeada em uma única passada | | |
| 210 | Pilha usando lista encadeada (mesma interface da pilha com array) | | |
| 211 | Vetor dinâmico (cresce sozinho, como uma lista, `ArrayList` ou `vector`) | | |
| 212 | Árvore binária de busca: inserir, buscar e percursos (em ordem, pré-ordem, pós-ordem) | | |
| 213 | Árvore binária de busca: altura, mínimo, máximo e contagem de nós | | |
| 214 | Árvore binária de busca: remover um nó | | |
| 215 | Verificar se uma árvore binária é uma BST válida | | |
| 216 | Tabela hash com tratamento de colisão por encadeamento | | |
| 217 | Heap mínimo e fila de prioridade | | |
| 218 | Trie para autocompletar | | |
| 219 | Grafo com lista de adjacência | | |
| 220 | Cache LRU | | |
| 221 | Calculadora de expressões pós-fixas (RPN) com pilha | | |
| 222 | Converter expressão infixa em pós-fixa (Shunting-yard) | | |
| 223 | Pilha que retorna o mínimo em O(1) | | |
| 224 | Fila implementada com duas pilhas | | |
| 225 | Desfazer/refazer (undo/redo) em um editor de texto simples usando duas pilhas | | |
| 226 | Histórico de navegação (voltar/avançar) como em um navegador | | |
| 227 | Playlist circular: próxima, anterior, remover, embaralhar | | |
| 228 | Fila de impressão com prioridade | | |

## 🔴 9. Arquivos e entrada/saída

| # | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| 229 | Ler um arquivo de texto e imprimir na tela com o número de cada linha | | |
| 230 | Contar linhas, palavras e caracteres de um arquivo (`wc`) | | |
| 231 | Copiar um arquivo para outro | | |
| 232 | Gravar números em um arquivo e depois ler e somar | | |
| 233 | Ler um CSV, imprimir como tabela e somar uma coluna numérica | | |
| 234 | Ordenar as linhas de um arquivo e gravar em outro | | |
| 235 | Procurar uma palavra em um arquivo e mostrar as linhas onde aparece (`grep`) | | |
| 236 | Ler argumentos da linha de comando (ex.: `./prog arquivo.txt 5`) | | |
| 237 | Ler da entrada padrão até o fim (EOF) e somar todos os números | | |
| 238 | Gravar um log com data e hora a cada execução do programa | | |
| 239 | Salvar e carregar uma lista de structs/objetos em arquivo binário | | |
| 240 | Mostrar as N últimas linhas de um arquivo (`tail`) | | |
| 241 | Contar a frequência de palavras de um arquivo e mostrar as 10 mais comuns | | |
| 242 | Remover linhas duplicadas de um arquivo | | |
| 243 | Comparar dois arquivos e mostrar as linhas diferentes (`diff` simples) | | |
| 244 | Ler um arquivo de configuração `chave=valor`, ignorando comentários e linhas em branco | | |
| 245 | Contar linhas de código, de comentários e em branco de um arquivo-fonte | | |
| 246 | Dividir um arquivo grande em partes de N linhas | | |
| 247 | Listar os arquivos de uma pasta com o tamanho de cada um | | |
| 248 | Tratar erros: o que acontece se o arquivo não existe ou não há permissão? Mostre uma mensagem amigável | | |

## 🔴 10. Structs, classes e orientação a objetos

> _Se a sua linguagem não tem classes, herança ou interfaces, use o recurso equivalente (structs + funções, traits, protocolos...) ou pule e anote o motivo._

| # | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| 249 | Definir uma `Pessoa` (nome, idade) e imprimir os dados | | |
| 250 | Fração com soma, multiplicação e simplificação automática | | |
| 251 | Relógio (hora, minuto, segundo) com `avancar(segundos)` que lida com o "vai um" entre as unidades | | |
| 252 | Conta bancária com depósito, saque e saldo (não permitir saldo negativo) | | |
| 253 | Hierarquia de formas (Círculo, Retângulo, Triângulo) com área e perímetro, usadas em uma lista polimórfica | | |
| 254 | Interface/contrato: vários meios de pagamento (cartão, pix, boleto) com o mesmo método `pagar()` | | |
| 255 | Baralho: classes `Carta` e `Baralho` com embaralhar e distribuir | | |
| 256 | Estacionamento: vagas, entrada e saída de carros, cobrança por tempo | | |
| 257 | Inventário de RPG com limite de peso e itens empilháveis | | |
| 258 | Biblioteca: livros, usuários, empréstimos, devoluções e multa por atraso | | |
| 259 | Tratamento de exceções: divisão por zero, entrada inválida, índice fora do limite | | |
| 260 | Criar sua própria exceção/erro (ex.: `SaldoInsuficiente`) | | |
| 261 | Tipo genérico/parametrizado (ex.: uma `Caixa` ou um `Par` que guarda qualquer tipo) | | |
| 262 | Implementar a conversão para texto e a comparação (igualdade e ordem) para suas classes, no estilo da sua linguagem | | |
| 263 | Encapsulamento: transforme uma classe com campos públicos em uma com validação (ex.: idade não pode ser negativa) | | |
| 264 | Composição vs. herança: modele um `Carro` que *tem* um `Motor` e depois refaça usando herança. Qual ficou melhor? | | |
| 265 | Cópia rasa vs. cópia profunda de um objeto que contém um array ou outro objeto | | |

## ⚫ 11. Mini projetos

| # | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| 266 | Jogo da velha (dois jogadores no terminal) | | |
| 267 | Jogo da velha contra o computador (que bloqueia e vence quando pode) | | |
| 268 | Jogo da forca | | |
| 269 | Mastermind: o computador escolhe 4 cores e dá dicas a cada tentativa | | |
| 270 | Wordle/Termo no terminal, com a lista de palavras em um arquivo | | |
| 271 | Campo minado jogável | | |
| 272 | Jogo da memória (pares de cartas) | | |
| 273 | Jogo 2048 | | |
| 274 | Jogo da cobrinha (Snake) | | |
| 275 | Batalha naval | | |
| 276 | Blackjack | | |
| 277 | Torre de Hanói jogável | | |
| 278 | Tetris simples | | |
| 279 | Roguelike minimalista: mapa, jogador, inimigos e itens | | |
| 280 | Simulador de dados de RPG com notação `2d6+3` | | |
| 281 | Sorteio de amigo secreto (ninguém tira a si mesmo; casais não se tiram) | | |
| 282 | Calculadora de linha de comando com histórico | | |
| 283 | Interpretador de expressões matemáticas (parênteses e precedência) | | |
| 284 | Interpretador de Brainfuck | | |
| 285 | Lista de tarefas (to-do) salva em arquivo | | |
| 286 | Agenda de contatos com busca por nome parcial | | |
| 287 | Agenda de consultas sem conflitos de horário | | |
| 288 | Controle de gastos pessoais (categorias e relatório mensal) | | |
| 289 | Sistema bancário com várias contas, transferências e extrato | | |
| 290 | Cadastro de alunos com notas, médias e relatórios | | |
| 291 | Quiz de perguntas e respostas lido de um arquivo | | |
| 292 | Reserva de assentos de cinema (mapa de assentos e sessões) | | |
| 293 | Sistema de votação com apuração e desempate | | |
| 294 | Gerador de labirinto aleatório e solucionador | | |
| 295 | Simulador de elevador | | |
| 296 | Simulador de caixa de supermercado com filas | | |
| 297 | Mini planilha (células e fórmulas simples de soma) | | |
| 298 | Banco de dados chave-valor persistido em arquivo (comandos SET, GET, DEL) | | |
| 299 | Mini shell (executa comandos do sistema) | | |
| 300 | Servidor TCP de eco (echo) e um cliente | | |
| 301 | Chat simples entre dois terminais usando sockets | | |
| 302 | Cliente HTTP que faz um GET e mostra a resposta | | |
| 303 | API REST simples com 3 rotas (GET, POST, DELETE) | | |
| 304 | Mini Git: salvar versões de um arquivo e voltar a uma anterior | | |

---

## 🏆 Placar

| Pessoa | Linguagem | Desafios concluídos |
|---|---|:---:|
| Dev 1 | | 0 |
| Dev 2 | | 0 |

## 💡 Ideias para continuar

- Resolver o mesmo desafio em uma **terceira linguagem** só para comparar.
- Criar desafios novos e mandar via Pull Request.
- Fazer uma competição: quem resolve mais desafios do mês?
- Comparar desempenho: rodem o mesmo algoritmo nas duas linguagens e meçam o tempo.
- Praticar em sites como Exercism, Advent of Code, Project Euler, LeetCode e Beecrowd.
