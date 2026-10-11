# 🧬 Desafios por Linguagem

Complemento do [`DESAFIOS.md`](DESAFIOS.md). Enquanto aquele arquivo tem desafios de lógica que servem para qualquer linguagem, este tem **574 desafios que exploram o que cada linguagem tem de específico**: ponteiros em C, geradores em Python, o event loop em JavaScript, o borrow checker em Rust, LINQ em C#, o sistema de tipos do TypeScript e as coleções e a JVM do Java.

## 📖 Como usar

1. Cada pessoa faz **os desafios da(s) própria(s) linguagem(ns)** e, se quiser, também os de outras linguagens para comparar.
2. Salve as soluções em `<linguagem>/especificos/` com o ID no nome do arquivo (ex.: `rust/especificos/RS-014.rs`, `python/especificos/PY-023.py`).
3. Marque ✅ na coluna de quem concluiu e faça *commits* pequenos (ex.: `PY-023: gerador de Fibonacci`).
4. Muitos desafios pedem para **provocar um erro de propósito** e entender a mensagem. Isso é parte do aprendizado, então não pule.
5. Quando um desafio disser "explique", escreva a explicação em um comentário no código ou em um `.md` ao lado.
6. A seção final tem **desafios entre linguagens**, para vocês dois fazerem em conjunto.

> 💡 Os desafios estão organizados por tema dentro de cada linguagem, do mais básico ao mais avançado. Itens marcados com uma versão (ex.: Java 21, .NET 8) dependem de uma versão recente da linguagem.

## 🗂️ Índice

- [🔩 C](#-c): 80 desafios
- [🐍 Python](#-python): 80 desafios
- [🟨 JavaScript](#-javascript): 80 desafios
- [☕ Java](#-java): 80 desafios
- [🟣 C# (C Sharp)](#-c-c-sharp): 80 desafios
- [🔷 TypeScript](#-typescript): 80 desafios
- [🦀 Rust](#-rust): 80 desafios
- [🔀 Desafios entre linguagens](#-desafios-entre-linguagens): 14 desafios

## 🔩 C

_Foco: ponteiros, memória manual, strings como arrays, structs/unions, pré-processador, bits, comportamento indefinido e programação de sistema._

### Ponteiros e endereços

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| C-001 | Declarar um `int`, imprimir o valor, o endereço (`&`) e o valor lido por um ponteiro (`*`) | | |
| C-002 | Função `trocar(int *a, int *b)` que troca as variáveis de quem chamou | | |
| C-003 | Função que devolve o mínimo e o máximo de um array usando parâmetros de saída (ponteiros) | | |
| C-004 | Percorrer um array usando só aritmética de ponteiros (sem `[]`) | | |
| C-005 | Mostrar que `arr[i]`, `*(arr + i)` e `i[arr]` são a mesma coisa e explicar por quê | | |
| C-006 | Mostrar que `sizeof(arr)` muda dentro de uma função que recebe o array como parâmetro (array decay) | | |
| C-007 | Ponteiro para ponteiro: função que aloca um array e o devolve por `int **` | | |
| C-008 | Ponteiros para função: calculadora com uma tabela (array) de operações | | |
| C-009 | `qsort` com função comparadora para `int`, strings e structs | | |
| C-010 | Implementar sua própria `bsearch` genérica com `void *` e ponteiro para função | | |
| C-011 | Função `trocar_generico(void *a, void *b, size_t tamanho)` usando `memcpy` | | |
| C-012 | `const` com ponteiros: escreva 4 declarações (`const int *`, `int * const`...) e veja o que o compilador recusa | | |
| C-013 | Diferença entre `char s[] = "abc"` e `char *s = "abc"`: tente modificar cada um e explique | | |
| C-014 | Matriz 2D de 3 formas: array estático, array de ponteiros e bloco único alocado; acessar nas 3 | | |
| C-015 | Imprimir endereços de variáveis locais, globais, `static` e alocadas com `malloc` e deduzir como a memória é organizada | | |

### Memória dinâmica

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| C-016 | Alocar um array com `malloc`, preencher, imprimir e liberar com `free` | | |
| C-017 | Refazer com `calloc` e mostrar a diferença para `malloc` | | |
| C-018 | Usar `realloc` em um array que cresce enquanto lê números até o EOF | | |
| C-019 | Criar um vazamento de memória de propósito, achá-lo com Valgrind ou AddressSanitizer e corrigir | | |
| C-020 | Provocar `use-after-free` e `double free` e ver como o ASan reporta | | |
| C-021 | Provocar um estouro de buffer na pilha e ver o que o ASan mostra | | |
| C-022 | Implementar `strdup` e `strndup` | | |
| C-023 | Implementar um alocador simples (arena / bump allocator) sobre um array grande | | |
| C-024 | Pilha genérica (`void *`) com `push`/`pop`, sem vazamentos | | |
| C-025 | Lista encadeada com todos os nós em `malloc` e uma função `liberar_lista` | | |
| C-026 | Desreferenciar `NULL`: o que acontece? Tratar corretamente o retorno de `malloc` | | |
| C-027 | Gerenciamento de memória por contagem de referências: struct com contador e funções `reter`/`soltar` | | |

### Strings

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| C-028 | Implementar `strlen`, `strcpy`, `strcat` e `strcmp` com ponteiros | | |
| C-029 | Implementar `memcpy` e `memmove` e mostrar por que `memcpy` falha com regiões que se sobrepõem | | |
| C-030 | Ler uma linha com segurança (`fgets`) e remover o `\n` do final | | |
| C-031 | Mostrar o perigo de `scanf("%s")` sem limite e corrigir | | |
| C-032 | Usar `strtok` para dividir uma linha CSV e explicar por que ela modifica a string original | | |
| C-033 | Implementar um `split` que devolve um array de strings alocadas dinamicamente | | |
| C-034 | Converter string em número com `strtol` tratando todos os erros (`errno`, `endptr`) | | |
| C-035 | Montar strings com `snprintf` sem estourar o buffer | | |
| C-036 | Contar quantos caracteres (não bytes) tem "ação" em UTF-8 | | |

### Structs, unions e enums

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| C-037 | `struct` aninhada com `typedef`; mostrar `sizeof` e `offsetof` de cada campo e o padding | | |
| C-038 | Reordenar os campos de uma struct para reduzir seu tamanho e comprovar com `sizeof` | | |
| C-039 | `union`: ver os bytes de um `float` como `uint32_t` e mostrar o padrão IEEE-754 | | |
| C-040 | Struct com *flexible array member* para guardar uma string de tamanho variável | | |
| C-041 | Bit-fields: empacotar uma data (dia, mês, ano) em 16 bits | | |
| C-042 | `enum` com `switch` e uma função que converte o enum em texto | | |
| C-043 | Tagged union: um "valor" que pode ser `int`, `double` ou string, com campo de tipo | | |
| C-044 | Passar struct por valor vs. por ponteiro: medir a diferença com uma struct grande | | |
| C-045 | Gravar um array de structs com `fwrite`/`fread` e discutir os problemas de portabilidade (padding, endianness) | | |

### Pré-processador e compilação

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| C-046 | Macro `MAX(a, b)`; mostrar o bug de `MAX(i++, j++)` e corrigir | | |
| C-047 | Macro `ARRAY_LEN(arr)` e mostrar por que falha quando recebe um ponteiro | | |
| C-048 | Include guards e `#pragma once`: dois headers que se incluem mutuamente e a solução | | |
| C-049 | Compilação condicional (`#ifdef`, `#if`): modo `DEBUG` e código por sistema operacional | | |
| C-050 | Macro variádica `LOG(fmt, ...)` usando `__FILE__` e `__LINE__` | | |
| C-051 | Stringification (`#x`) e concatenação (`##`): macro `PRINT_VAR(x)` | | |
| C-052 | X-macros: gerar um enum e uma tabela de nomes a partir de uma lista só | | |
| C-053 | Dividir um programa em vários `.c`/`.h` com funções `static` e variável `extern` | | |
| C-054 | Escrever um `Makefile` que compila vários arquivos com `-Wall -Wextra -Werror` | | |
| C-055 | Compilar com `-fsanitize=address,undefined` e corrigir todos os avisos de um programa propositalmente bugado | | |
| C-056 | Criar uma biblioteca estática (`.a`) e uma dinâmica (`.so`) e linkar nas duas formas | | |

### Bits, tipos e comportamento indefinido

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| C-057 | Funções para ligar, desligar, alternar e testar o bit N de um número | | |
| C-058 | Contar bits 1 (popcount) de 3 formas: laço, truque de Kernighan e tabela | | |
| C-059 | Inverter a ordem dos bits de um `uint8_t` | | |
| C-060 | Detectar endianness com ponteiro e com `union` | | |
| C-061 | Overflow de `signed` vs. `unsigned`: por que o primeiro é comportamento indefinido | | |
| C-062 | Promoção de inteiros: explicar `-1 < 1u` e `(unsigned char)200 + (unsigned char)100` | | |
| C-063 | Usar `<stdint.h>` e `<inttypes.h>` para imprimir `uint64_t` corretamente | | |
| C-064 | Mostrar por que `0.1 + 0.2 == 0.3` é falso e comparar floats com epsilon | | |
| C-065 | Listar 5 exemplos de comportamento indefinido e mostrar um que muda de resultado entre `-O0` e `-O2` | | |

### Arquivos, processos e sistema

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| C-066 | Ler um arquivo binário em blocos com `fread` e calcular um checksum | | |
| C-067 | Usar `fseek`/`ftell` para descobrir o tamanho de um arquivo e ler seus últimos N bytes | | |
| C-068 | Tratar flags com `getopt` (ex.: `-n 5 -v arquivo`) | | |
| C-069 | `fork` + `exec` + `wait` (Unix): executar um comando e pegar o código de saída | | |
| C-070 | Comunicação entre pai e filho com `pipe` | | |
| C-071 | Capturar `SIGINT` (Ctrl+C) e encerrar liberando recursos | | |
| C-072 | Somar um array em 4 threads com `pthread` | | |
| C-073 | Provocar uma race condition com `pthread` e corrigir com mutex | | |
| C-074 | `setjmp`/`longjmp` para um tratamento de erro simples | | |
| C-075 | Medir tempo com `clock()` e `clock_gettime` | | |

### Idiomas de C

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| C-076 | Vetor dinâmico genérico usando macros | | |
| C-077 | Hash map com chaves string | | |
| C-078 | "Orientação a objetos" em C: struct com ponteiros para função (vtable) simulando polimorfismo | | |
| C-079 | `printf` simplificado com `stdarg.h` (suportando `%d`, `%s` e `%c`) | | |
| C-080 | Parser de linha de comando de um mini shell que entende aspas | | |

## 🐍 Python

_Foco: jeito "pythônico", comprehensions, geradores, decoradores, protocolos (métodos dunder), dataclasses, tipagem, biblioteca padrão e concorrência._

### Idiomático e armadilhas

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| PY-001 | Trocar variáveis com desempacotamento de tupla; depois usar desempacotamento estendido (`a, *resto = lista`) | | |
| PY-002 | Fatiamento (slicing): inverter lista, pegar de 2 em 2, últimos 3 e copiar, tudo com `[::]` | | |
| PY-003 | Slicing com atribuição: substituir, inserir e remover trechos de uma lista | | |
| PY-004 | f-strings com formatação (`:>10`, `:.2f`, `:,`, `=`) para imprimir uma tabela de produtos | | |
| PY-005 | `is` vs. `==`: mostrar o cache de inteiros pequenos e o interning de strings | | |
| PY-006 | O bug do argumento padrão mutável (`def f(x=[])`) e como corrigir | | |
| PY-007 | Aliasing: mostrar que `b = a` não copia; usar `copy` e `deepcopy`; o bug de `[[0] * 3] * 3` | | |
| PY-008 | Operador walrus (`:=`) em um laço de leitura e dentro de uma comprehension | | |
| PY-009 | `match`/`case` (pattern matching estrutural) para interpretar comandos como `["mover", x, y]` | | |
| PY-010 | Comparações encadeadas (`1 < x < 10`), `any` e `all` | | |
| PY-011 | `enumerate`, `zip`, `zip_longest` e `reversed`: processar duas listas paralelas sem índices | | |
| PY-012 | `sorted` com `key`: ordenar por idade decrescente e nome crescente | | |
| PY-013 | `Decimal` e `Fraction`: mostrar `0.1 + 0.2` e a versão correta | | |
| PY-014 | Parâmetros somente posicionais (`/`), somente nomeados (`*`), `*args` e `**kwargs` | | |
| PY-015 | EAFP vs. LBYL: resolver o mesmo problema com `try/except` e com `if` | | |

### Comprehensions e estilo funcional

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| PY-016 | List comprehension: quadrados dos pares; depois a versão com `map`/`filter` | | |
| PY-017 | Dict e set comprehension: inverter um dicionário e agrupar palavras por tamanho | | |
| PY-018 | Comprehension aninhada: achatar e transpor uma matriz em uma linha | | |
| PY-019 | `functools.reduce` e `partial`: criar `dobro` e `potencia_de_2` a partir de `pow` | | |
| PY-020 | Closures: contador com `nonlocal`; o bug clássico de closures em laço e a correção | | |

### Geradores e iteradores

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| PY-021 | Gerador infinito de Fibonacci com `yield`, usando `itertools.islice` | | |
| PY-022 | Gerador que lê um arquivo enorme linha a linha sem carregá-lo na memória | | |
| PY-023 | Classe iterável com `__iter__`/`__next__` e depois com gerador | | |
| PY-024 | `yield from`: percorrer uma árvore recursivamente | | |
| PY-025 | Comparar uso de memória de lista vs. expressão geradora (`sys.getsizeof`) | | |
| PY-026 | `send()` em geradores: corrotina que calcula média móvel | | |
| PY-027 | `itertools`: `product`, `permutations`, `combinations`, `groupby`, `chain`, `accumulate`, `cycle`; um problema para cada | | |
| PY-028 | Pipeline de geradores encadeados (ler, filtrar, transformar, somar) | | |

### Decoradores e context managers

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| PY-029 | Decorador `@cronometrar` que mede o tempo de uma função | | |
| PY-030 | Decorador com argumentos: `@repetir(3)` | | |
| PY-031 | Decorador `@memoizar` e comparação com `functools.lru_cache` | | |
| PY-032 | Mostrar o que se perde sem `functools.wraps` | | |
| PY-033 | Decorador que registra funções em um dicionário (registro de plugins) | | |
| PY-034 | Context manager com `__enter__`/`__exit__` para medir tempo ou gerenciar um recurso | | |
| PY-035 | Context manager com `@contextmanager` e `yield` | | |

### Classes e protocolos (dunder)

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| PY-036 | `__repr__` vs. `__str__`: quando cada um aparece | | |
| PY-037 | Sobrecarga de operadores: `Vetor` com `+`, `-`, `*`, `==`, `abs` e `__bool__` | | |
| PY-038 | `__getitem__`, `__len__` e `__contains__`: uma classe que se comporta como sequência | | |
| PY-039 | `__call__`: objeto que funciona como função | | |
| PY-040 | `@property` com validação (getter, setter e deleter) | | |
| PY-041 | `@classmethod` e `@staticmethod`: construtor alternativo `from_string` | | |
| PY-042 | `__slots__`: comparar uso de memória | | |
| PY-043 | `@dataclass`: `frozen`, `order`, `field(default_factory=...)` e `__post_init__` | | |
| PY-044 | `NamedTuple` vs. `dataclass` vs. `dict`: modelar o mesmo dado das três formas | | |
| PY-045 | Herança múltipla e MRO: problema do diamante, `__mro__` e `super()` | | |
| PY-046 | Mixins: `JsonMixin` e `ComparableMixin` | | |
| PY-047 | `abc.ABC`: classe abstrata com métodos abstratos; tentar instanciar | | |
| PY-048 | `typing.Protocol`: duck typing verificado por tipo | | |
| PY-049 | Descritor `Positivo` que valida atributos | | |
| PY-050 | Metaclasse simples que registra todas as subclasses; depois refazer com `__init_subclass__` | | |
| PY-051 | `Enum`, `IntEnum`, `Flag` e `auto()`: modelar permissões de arquivo | | |
| PY-052 | `__eq__` e `__hash__`: usar objetos como chave de dicionário e em `set` | | |

### Tipagem

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| PY-053 | Anotar funções (`list[int]`, `dict[str, int]`, `X \| None`) e rodar o `mypy` | | |
| PY-054 | `TypedDict` e `Literal` para modelar o JSON de uma API | | |
| PY-055 | `Generic[T]` e `TypeVar`: pilha genérica tipada | | |
| PY-056 | `Callable` e `ParamSpec`: tipar um decorador corretamente | | |

### Biblioteca padrão

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| PY-057 | `Counter`: as 10 palavras mais frequentes de um texto | | |
| PY-058 | `defaultdict`: agrupar e contar sem `if chave in` | | |
| PY-059 | `deque` com `maxlen`: manter as últimas N linhas de um log | | |
| PY-060 | `heapq`: fila de prioridade e top-K | | |
| PY-061 | Operações de `set` (`\|`, `&`, `-`, `^`) para comparar listas de convidados | | |
| PY-062 | `pathlib`: listar recursivamente todos os `.py` e somar os tamanhos | | |
| PY-063 | `csv` e `json`: converter CSV para JSON e de volta | | |
| PY-064 | `argparse`: CLI com subcomandos (`add`, `list`, `done`) | | |
| PY-065 | `logging` com níveis, formato e arquivo rotativo | | |
| PY-066 | `re`: extrair e-mails, telefones e datas com grupos nomeados | | |
| PY-067 | `datetime` e `zoneinfo`: diferença entre datas com fusos horários | | |
| PY-068 | `subprocess`: executar um comando, capturar a saída e tratar erros | | |
| PY-069 | `sqlite3`: CRUD completo | | |
| PY-070 | `pytest`: testes parametrizados; `doctest` | | |
| PY-071 | `timeit` e `cProfile`: medir e otimizar uma função lenta | | |

### Concorrência

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| PY-072 | `threading`: baixar várias páginas em paralelo e medir; mostrar o efeito do GIL em tarefa CPU-bound | | |
| PY-073 | `multiprocessing.Pool`: paralelizar uma tarefa CPU-bound | | |
| PY-074 | `asyncio`: `gather` de várias corrotinas com `sleep`; produtor/consumidor com `asyncio.Queue` | | |
| PY-075 | `asyncio` com `httpx`/`aiohttp`: requisições concorrentes com timeout | | |

### Pacotes e ambiente

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| PY-076 | Criar um virtualenv, instalar um pacote e gerar `requirements.txt`/`pyproject.toml` | | |
| PY-077 | Criar um pacote com `__init__.py`, `__all__` e imports relativos | | |
| PY-078 | `if __name__ == "__main__":` — um módulo que serve como biblioteca e como script | | |
| PY-079 | Exceções: `try/except/else/finally`, `raise ... from`, exceção própria e `ExceptionGroup` | | |
| PY-080 | One-liners: FizzBuzz, achatar lista, transposta e palíndromo em uma linha | | |

## 🟨 JavaScript

_Foco: tipos e coerção, `this`, closures, protótipos, event loop e assíncrono, Node.js e DOM._

### Tipos, coerção e armadilhas

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| JS-001 | Tabela de `typeof` para vários valores (`null`, `NaN`, `[]`, funções...) e explicar os surpreendentes | | |
| JS-002 | `==` vs. `===`: montar uma tabela de pares e prever o resultado antes de rodar | | |
| JS-003 | Explicar `[] + []`, `[] + {}`, `"5" - 2`, `"5" + 2` e `true + 1` | | |
| JS-004 | `NaN !== NaN`: `Number.isNaN` vs. `isNaN` vs. `Object.is` | | |
| JS-005 | `0.1 + 0.2`: resolver com `toFixed`, `Number.EPSILON` e centavos inteiros | | |
| JS-006 | `BigInt`: calcular 50! e comparar com `Number` | | |
| JS-007 | `var` vs. `let` vs. `const`: hoisting, zona morta temporal e o bug de `var` com `setTimeout` em laço | | |
| JS-008 | `const` com objeto: mutar vs. `Object.freeze` (raso) vs. freeze profundo | | |
| JS-009 | Falsy/truthy e a diferença entre `\|\|`, `??` e `?.` | | |
| JS-010 | Template literals e *tagged templates*: tag que escapa HTML | | |
| JS-011 | Métodos de string e `Intl`: `padStart`, `at`, `replaceAll`, `localeCompare`, `Intl.NumberFormat` e `Intl.DateTimeFormat` em pt-BR | | |
| JS-012 | Armadilhas de `Date`: mês começa em 0, parse de strings e UTC vs. local | | |

### Funções, `this` e closures

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| JS-013 | Declaração, expressão e arrow function: hoisting e `this` em cada uma | | |
| JS-014 | Prever o valor de `this` em 8 situações (método, callback, arrow, `new`, `call`/`apply`/`bind`, evento) | | |
| JS-015 | Implementar sua versão de `bind`, `call` e `apply` | | |
| JS-016 | Closure: contador privado e módulo com estado privado (IIFE) | | |
| JS-017 | `curry(fn)` genérico | | |
| JS-018 | `compose` e `pipe` | | |
| JS-019 | `debounce` e `throttle` | | |
| JS-020 | `memoize` com `Map` | | |
| JS-021 | Parâmetros padrão, rest, spread e objeto de opções com desestruturação | | |
| JS-022 | Reimplementar `map`, `filter`, `reduce`, `flat`, `some` e `every` | | |
| JS-023 | Recursão com *trampolim* para evitar estouro de pilha | | |

### Arrays, objetos e coleções

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| JS-024 | Desestruturação aninhada com valores padrão e renomeação | | |
| JS-025 | Spread: clonar e mesclar objetos/arrays (e mostrar que a cópia é rasa) | | |
| JS-026 | `structuredClone` vs. `JSON.parse(JSON.stringify(x))`: o que cada um perde (`Date`, `undefined`, `Map`, ciclos) | | |
| JS-027 | `Object.entries`/`fromEntries`/`assign`: transformar um objeto (ex.: dobrar todos os preços) | | |
| JS-028 | `reduce` para agrupar por propriedade (groupBy) e contar frequências | | |
| JS-029 | Por que `[10, 9, 1].sort()` dá errado; comparador correto e ordenação estável | | |
| JS-030 | `flat` e `flatMap`: transformar uma lista de pedidos em lista de itens | | |
| JS-031 | `Map`, `Set`, `WeakMap`, `WeakSet`: quando usar em vez de objeto/array | | |
| JS-032 | `WeakRef` e `FinalizationRegistry`: um cache que não impede a coleta de lixo | | |
| JS-033 | Arrays esparsos: `new Array(3)` vs. `Array.from({ length: 3 })` e o que `forEach` pula | | |
| JS-034 | `for...in` vs. `for...of` vs. `forEach` vs. `for`: tabela de diferenças | | |
| JS-035 | Ordem das chaves de um objeto (números primeiro): demonstrar | | |
| JS-036 | Implementar `deepEqual` para comparar objetos | | |
| JS-037 | `Object.defineProperty`: `enumerable`, `writable`, `configurable`; getters/setters em objetos literais | | |
| JS-038 | `Symbol`: chave "privada", `Symbol.iterator` e `Symbol.toPrimitive` | | |
| JS-039 | Objeto iterável com `Symbol.iterator`; depois com gerador | | |
| JS-040 | Geradores (`function*`): `yield`, `return`, `throw`; gerador de IDs e de Fibonacci | | |

### Protótipos e classes

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| JS-041 | Cadeia de protótipos com `Object.create`: criar objetos e mostrar a cadeia | | |
| JS-042 | Função construtora e `prototype`: herança "à moda antiga" | | |
| JS-043 | `class`, `extends`, `super`, `static`, campos privados `#x` e getters | | |
| JS-044 | Provar que `class` é açúcar sintático sobre protótipos | | |
| JS-045 | Mixins com `Object.assign` e com funções de classe | | |
| JS-046 | `instanceof` vs. `getPrototypeOf` vs. duck typing | | |
| JS-047 | `Proxy`: objeto que valida atribuições e registra leituras; array com índices negativos | | |
| JS-048 | `toString`, `valueOf` e `toJSON`: controlar as conversões do seu objeto | | |

### Assíncrono

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| JS-049 | Event loop: prever a ordem de saída de `setTimeout`, `Promise.then`, `queueMicrotask`, `process.nextTick` e código síncrono | | |
| JS-050 | Reproduzir o "callback hell" e refatorar para Promises e depois para `async/await` | | |
| JS-051 | Implementar `sleep(ms)` com Promise | | |
| JS-052 | Criar sua própria `MyPromise` com `then` e `catch` | | |
| JS-053 | `Promise.all`, `allSettled`, `race` e `any`: um caso real para cada | | |
| JS-054 | Tratamento de erros: `try/catch` com `await`, `.catch` e rejeições não tratadas | | |
| JS-055 | Limitador de concorrência: executar N tarefas assíncronas com no máximo K ao mesmo tempo | | |
| JS-056 | Retry com backoff exponencial | | |
| JS-057 | Timeout e cancelamento com `AbortController` | | |
| JS-058 | `for await...of` com gerador assíncrono (paginação de uma API) | | |
| JS-059 | `fetch` em uma API pública tratando status HTTP e erros de rede | | |
| JS-060 | `EventEmitter` do Node: chat simples; depois implementar o seu próprio | | |

### Node.js

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| JS-061 | ES Modules vs. CommonJS: criar uma lib nos dois formatos e importar | | |
| JS-062 | `import()` dinâmico e `export default` vs. nomeado | | |
| JS-063 | `process.argv` e `readline`: CLI interativa | | |
| JS-064 | `fs/promises`: ler, escrever e observar arquivos (`watch`) | | |
| JS-065 | Streams: copiar e transformar um arquivo grande linha a linha (`Transform`) | | |
| JS-066 | `http` puro: servidor com roteamento manual; depois com Express ou Fastify | | |
| JS-067 | `child_process`: executar um comando e capturar a saída | | |
| JS-068 | `worker_threads`: tarefa pesada fora da thread principal | | |
| JS-069 | `npm`: `package.json`, scripts, dependências de desenvolvimento e `npm link` | | |
| JS-070 | Testes com `node:test` ou Jest | | |
| JS-071 | `JSON.stringify` com `replacer` e `JSON.parse` com `reviver`: serializar `Date` e `Map` | | |
| JS-072 | `RegExp`: grupos nomeados, lookahead/lookbehind e flags | | |

### Browser e DOM

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| JS-073 | Lista de tarefas dinâmica com delegação de eventos | | |
| JS-074 | `localStorage`: persistir a lista de tarefas | | |
| JS-075 | `fetch` + DOM: buscar dados e renderizar cards | | |
| JS-076 | Event bubbling vs. capturing: demonstrar com 3 elementos aninhados | | |
| JS-077 | `IntersectionObserver`: lazy load ou scroll infinito | | |
| JS-078 | `requestAnimationFrame`: animar uma bolinha quicando em um `<canvas>` | | |
| JS-079 | Web Component com Shadow DOM: criar `<meu-botao>` | | |
| JS-080 | Drag and drop com a API nativa | | |

## ☕ Java

_Foco: tipos e wrappers, `equals`/`hashCode`, coleções, generics, interfaces e records, streams, concorrência, JVM e ecossistema (Maven/Gradle). Alguns itens exigem Java 17 ou 21._

### Fundamentos da linguagem

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| JAVA-001 | Primitivos vs. wrappers e autoboxing: `Integer == Integer` com 127 e com 128 | | |
| JAVA-002 | `String` imutável e o *string pool*: `==` vs. `equals` e `intern()` | | |
| JAVA-003 | `StringBuilder` vs. concatenação em laço: medir | | |
| JAVA-004 | Text blocks, `String.format`, `formatted`, `strip`, `repeat` e `isBlank` | | |
| JAVA-005 | `var` (inferência local): onde pode e onde não pode | | |
| JAVA-006 | `Arrays`: `toString`, `deepToString`, `sort`, `fill`, `copyOf`, `asList`; array de arrays irregular | | |
| JAVA-007 | Passagem por valor: demonstrar que Java sempre passa por valor, mesmo com objetos | | |
| JAVA-008 | Sobrecarga e sobrescrita: prever qual método é chamado com autoboxing e varargs | | |
| JAVA-009 | Ordem de inicialização: prever a saída com herança, blocos `static` e blocos de instância | | |
| JAVA-010 | `static`, `final` e `static final`: usos e armadilhas | | |
| JAVA-011 | Modificadores de acesso (`public`, `protected`, padrão, `private`) em pacotes diferentes: montar uma tabela testando cada um | | |
| JAVA-012 | Classes internas, estáticas, locais e anônimas: um exemplo de cada | | |
| JAVA-013 | Classe imutável (campos `final`, cópias defensivas) | | |
| JAVA-014 | `clone()`: cópia rasa, cópia profunda e por que muita gente prefere um construtor de cópia | | |

### Igualdade, ordenação e coleções

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| JAVA-015 | Implementar `equals` e `hashCode` e mostrar o bug em um `HashSet` quando só um deles é sobrescrito | | |
| JAVA-016 | `Comparable` vs. `Comparator` (`thenComparing`, `reversed`) | | |
| JAVA-017 | `ArrayList` vs. `LinkedList`: medir inserção, remoção e acesso | | |
| JAVA-018 | `HashMap`, `LinkedHashMap` e `TreeMap`: ordem de iteração de cada um | | |
| JAVA-019 | `HashSet`, `TreeSet`, `ArrayDeque` e `PriorityQueue`: um problema para cada | | |
| JAVA-020 | `Iterator`: remover durante a iteração e provocar `ConcurrentModificationException` | | |
| JAVA-021 | `Iterable` e `for-each`: tornar uma classe sua iterável e usá-la em `for (x : obj)` | | |
| JAVA-022 | `List.of`, `Map.of`, `Set.of`: coleções imutáveis e o que acontece ao modificar | | |
| JAVA-023 | `Collections`: `unmodifiableList`, `shuffle`, `frequency`, `nCopies` | | |
| JAVA-024 | `EnumMap` e `EnumSet` | | |

### Generics e tipos modernos

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| JAVA-025 | Classe genérica `Par<A, B>` e método genérico `<T extends Comparable<T>> T max(...)` | | |
| JAVA-026 | Wildcards `? extends` vs. `? super` (PECS): copiar entre listas | | |
| JAVA-027 | Type erasure: demonstrar por que não dá `new T[]` nem `instanceof List<String>` | | |
| JAVA-028 | Interfaces com métodos `default` e `static` | | |
| JAVA-029 | Classe abstrata vs. interface: modelar o mesmo problema das duas formas | | |
| JAVA-030 | `enum` com campos, métodos e comportamento por constante | | |
| JAVA-031 | `record`: construtor compacto com validação e comparação com uma classe manual | | |
| JAVA-032 | `sealed` interfaces + `switch` com pattern matching exaustivo | | |
| JAVA-033 | Pattern matching com `instanceof` e `switch` com guardas (`when`) | | |
| JAVA-034 | Switch expressions (`->` e `yield`) | | |
| JAVA-035 | `Optional`: refatorar verificações de `null` (`map`, `flatMap`, `orElseGet`) e por que não usar em campos | | |

### Exceções

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| JAVA-036 | Checked vs. unchecked: criar as duas e mostrar a diferença na assinatura dos métodos | | |
| JAVA-037 | `try-with-resources` com uma classe `AutoCloseable` sua e a ordem de fechamento | | |
| JAVA-038 | Multi-catch, `finally` e exceções suprimidas (`suppressed`) | | |
| JAVA-039 | Exceção customizada com causa (`cause`) e leitura do stack trace | | |

### Lambdas e Streams

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| JAVA-040 | Interfaces funcionais: `Predicate`, `Function`, `Supplier`, `Consumer`, `BiFunction` e a sua própria com `@FunctionalInterface` | | |
| JAVA-041 | Referências a métodos (`Classe::metodo`): os 4 tipos | | |
| JAVA-042 | Streams: `filter`, `map`, `sorted`, `distinct`, `limit`, `skip`, `flatMap`, `reduce`, `peek` | | |
| JAVA-043 | `Collectors`: `groupingBy`, `partitioningBy`, `counting`, `joining`, `toMap`, `summarizingInt` | | |
| JAVA-044 | Reimplementar `groupingBy` manualmente e comparar | | |
| JAVA-045 | Streams infinitos (`iterate`, `generate`) com `limit`; `takeWhile` e `dropWhile` | | |
| JAVA-046 | `IntStream`, `range` e `boxed`; `Collectors.teeing` | | |
| JAVA-047 | Stream paralelo: medir e achar um caso em que piora | | |

### Concorrência

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| JAVA-048 | `Thread` e `Runnable`: iniciar, `join`, `sleep` e `interrupt` | | |
| JAVA-049 | Race condition em um contador compartilhado; corrigir com `synchronized`, `AtomicInteger` e `ReentrantLock` | | |
| JAVA-050 | `volatile`: demonstrar uma flag que outra thread não enxerga | | |
| JAVA-051 | Deadlock proposital e correção por ordenação de locks | | |
| JAVA-052 | `ExecutorService` e `Future`: executar tarefas e coletar resultados | | |
| JAVA-053 | `CompletableFuture`: encadear, combinar e tratar erros | | |
| JAVA-054 | `ConcurrentHashMap` e `BlockingQueue`: produtor/consumidor | | |
| JAVA-055 | `CountDownLatch`, `Semaphore` e `CyclicBarrier`: um caso para cada | | |
| JAVA-056 | Virtual threads (Java 21): criar 100 mil e comparar com threads de plataforma | | |
| JAVA-057 | `ThreadLocal`: contexto por thread | | |

### JVM, memória e reflexão

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| JAVA-058 | Observar o coletor de lixo (`-verbose:gc`, VisualVM ou jconsole) criando objetos em laço | | |
| JAVA-059 | Provocar `OutOfMemoryError` e `StackOverflowError` e explicar a diferença | | |
| JAVA-060 | `WeakReference` e `SoftReference`: um cache que libera sob pressão de memória | | |
| JAVA-061 | Vazamento de memória clássico (listener ou campo estático) e como achá-lo | | |
| JAVA-062 | Reflexão: listar métodos e campos, invocar método por nome e ler campo privado | | |
| JAVA-063 | Criar a anotação `@Validar` e processá-la por reflexão | | |
| JAVA-064 | `java.lang.reflect.Proxy`: proxy dinâmico que registra as chamadas | | |
| JAVA-065 | `Serializable`, `transient` e `serialVersionUID` | | |
| JAVA-066 | `jshell`: resolver 10 desafios simples do `DESAFIOS.md` no REPL | | |

### Biblioteca e ecossistema

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| JAVA-067 | `java.nio.file` (`Files`, `Path`): ler, escrever e percorrer diretórios | | |
| JAVA-068 | `Scanner` vs. `BufferedReader`: ler entrada grande rapidamente | | |
| JAVA-069 | `java.time`: `LocalDate`, `Duration`, `Period` e `ZonedDateTime`; calcular idade e fuso | | |
| JAVA-070 | `BigInteger` e `BigDecimal`: fatorial de 100 e dinheiro sem erro de arredondamento | | |
| JAVA-071 | `Math.addExact`, `multiplyExact` e `floorMod`: detectar overflow de forma segura | | |
| JAVA-072 | `HttpClient`: GET e POST e leitura de JSON | | |
| JAVA-073 | `ProcessBuilder`: executar um comando externo e ler sua saída e seu código de saída | | |
| JAVA-074 | Servidor de chat multi-thread com sockets | | |
| JAVA-075 | `ResourceBundle`: internacionalização com pt_BR e en_US | | |
| JAVA-076 | JDBC com SQLite ou H2: CRUD | | |
| JAVA-077 | JUnit 5: testes parametrizados, `assertThrows` e um mock com Mockito | | |
| JAVA-078 | Maven ou Gradle: projeto com dependências e testes; gerar um JAR executável | | |
| JAVA-079 | Módulos (JPMS): criar um `module-info.java` | | |
| JAVA-080 | Padrões que ficam bonitos em Java: Builder, Strategy com lambdas e Singleton com `enum` | | |

## 🟣 C# (C Sharp)

_Foco: tipos valor vs. referência, propriedades, records e pattern matching, LINQ, delegates/eventos, async/await, `Span<T>`, ecossistema .NET. Alguns itens exigem .NET 8 ou superior._

### Fundamentos da linguagem

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| CS-001 | `dotnet new console`, `run`, `build` e `test`; top-level statements vs. `Main` | | |
| CS-002 | `struct` vs. `class`: modificar a cópia e o original; `ref`, `out` e `in` | | |
| CS-003 | Boxing e unboxing: medir o custo com `ArrayList` vs. `List<int>` | | |
| CS-004 | `string` imutável, `StringBuilder`, interpolação com formato (`{x:N2}`, `{d:yyyy-MM-dd}`), raw string literals e `@""` | | |
| CS-005 | `StringComparison` e cultura: `ToUpper` vs. `ToUpperInvariant` | | |
| CS-006 | `int?`: `??`, `??=`, `?.` e `HasValue` | | |
| CS-007 | Nullable reference types (`#nullable enable`): corrigir todos os avisos de um código | | |
| CS-008 | `decimal` vs. `double` para dinheiro; `checked` e `unchecked` | | |
| CS-009 | `DateTime` vs. `DateTimeOffset` vs. `DateOnly`/`TimeOnly` | | |
| CS-010 | Tuplas nomeadas e desconstrução; retorno de múltiplos valores | | |
| CS-011 | `params`, parâmetros opcionais e nomeados: criar `Somar(params int[] n)` e a armadilha do valor padrão em bibliotecas | | |
| CS-012 | `ValueTuple` vs. `Tuple`: usar tuplas como chave de `Dictionary` | | |
| CS-013 | `enum` e `[Flags]`: permissões com operações bit a bit; `Enum.TryParse` | | |

### Propriedades e tipos

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| CS-014 | Auto-properties, `init`, `required` e propriedades calculadas | | |
| CS-015 | Indexadores: `this[int i]` e `this[string chave]` | | |
| CS-016 | Sobrecarga de operadores e conversões implícitas/explícitas (`Dinheiro` ou `Fracao`) | | |
| CS-017 | `record` e `record struct`: igualdade por valor, `with` e desconstrução | | |
| CS-018 | `init`, `with` e imutabilidade: modelar um `Pedido` imutável e gerar versões alteradas | | |
| CS-019 | Pattern matching: de tipo, de propriedade, relacional, `and`/`or`/`not` e list patterns; `switch` expressions | | |
| CS-020 | `is`, `as` e cast: diferenças e exceções | | |
| CS-021 | Interface com implementação padrão e implementação explícita de interface | | |
| CS-022 | `virtual`, `override`, `new` e `sealed`: prever a saída do ocultamento com `new` | | |
| CS-023 | Classes `partial`, métodos parciais e classes `static` | | |
| CS-024 | Extension methods: criar `StringExtensions` e `EnumerableExtensions` | | |
| CS-025 | Genéricos com restrições (`where T : class, new()`, `IComparable<T>`); covariância e contravariância (`out`/`in`) | | |
| CS-026 | Matemática genérica (`INumber<T>`): escrever `Somar<T>` que funciona para qualquer tipo numérico | | |
| CS-027 | `IEquatable<T>`, `IComparable<T>` e `GetHashCode` com `HashCode.Combine` | | |
| CS-028 | `StringComparer` e `IComparer<T>`: ordenar texto com cultura, ordinal e ignorando maiúsculas, e ver como o resultado muda | | |

### Delegates, eventos e LINQ

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| CS-029 | Delegates: `Action`, `Func` e `Predicate`; delegate multicast | | |
| CS-030 | `event` e `EventHandler<T>`: classe `Termostato` que dispara eventos | | |
| CS-031 | Lambdas e closures: capturar a variável de `for` vs. `foreach` | | |
| CS-032 | LINQ (métodos): `Where`, `Select`, `SelectMany`, `GroupBy`, `OrderBy/ThenBy`, `Join`, `Aggregate`, `Zip`, `Chunk` | | |
| CS-033 | LINQ (sintaxe de query): a mesma consulta nas duas sintaxes | | |
| CS-034 | Execução adiada (*deferred execution*): mostrar o bug da enumeração múltipla e `ToList()` | | |
| CS-035 | Implementar suas versões de `Where`, `Select` e `Take` com `yield return` | | |
| CS-036 | Gerador infinito de números primos com `yield return` e consumo com `Take` | | |
| CS-037 | `IEnumerable<T>` manual vs. `yield`; `IAsyncEnumerable<T>` | | |
| CS-038 | `Dictionary`, `HashSet`, `SortedDictionary`, `Queue`, `Stack`, `LinkedList` e `PriorityQueue`: um problema para cada | | |
| CS-039 | Coleções imutáveis: `ReadOnlyCollection`, `ImmutableList` e `FrozenDictionary` | | |

### Exceções, recursos e memória

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| CS-040 | `try/catch/when/finally`; `throw;` vs. `throw ex;` (stack trace); exceção customizada; `AggregateException` | | |
| CS-041 | `IDisposable` e `using`: padrão Dispose completo e finalizador; `await using` | | |
| CS-042 | Coleta de lixo: forçar `GC.Collect`, `WeakReference`, gerações e medir alocações | | |
| CS-043 | `Span<T>` e `Memory<T>`: fatiar array e string sem alocar; benchmark com BenchmarkDotNet | | |
| CS-044 | Comparar `string +`, `StringBuilder` e `string.Create` medindo tempo e alocações (BenchmarkDotNet) | | |
| CS-045 | `stackalloc` e `ArrayPool<T>` | | |
| CS-046 | `unsafe` e `fixed`: somar um array com ponteiros | | |
| CS-047 | `ref struct` e `ref return` | | |
| CS-048 | `Lazy<T>`: inicialização preguiçosa e thread-safe | | |
| CS-049 | P/Invoke: chamar uma função de uma DLL ou `.so` nativa | | |

### Assíncrono e concorrência

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| CS-050 | `async/await`: baixar 5 URLs concorrentemente com `Task.WhenAll`; `WhenAny` | | |
| CS-051 | `Task` vs. `Thread`; `Task.Run`; `ConfigureAwait`; deadlock com `.Result` | | |
| CS-052 | `CancellationToken`: cancelar uma operação longa e usar timeout | | |
| CS-053 | `Parallel.For`/`ForEach` e PLINQ: medir; criar race condition e corrigir com `lock` ou `Interlocked` | | |
| CS-054 | `lock`, `Monitor`, `SemaphoreSlim` e `ReaderWriterLockSlim` | | |
| CS-055 | `ConcurrentDictionary` e `ConcurrentQueue`: contador de palavras paralelo | | |
| CS-056 | `System.Threading.Channels`: produtor/consumidor | | |
| CS-057 | `ValueTask` vs. `Task` | | |
| CS-058 | `IProgress<T>`: relatório de progresso | | |
| CS-059 | `PeriodicTimer`: tarefa periódica | | |

### Reflexão e metaprogramação

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| CS-060 | Reflexão: listar propriedades e invocar métodos por nome | | |
| CS-061 | Atributo `[Validar]` próprio e um validador que o lê | | |
| CS-062 | `CallerMemberName`, `CallerFilePath` e `CallerLineNumber` | | |
| CS-063 | Expression trees: construir `x => x.Idade > 18` em runtime e compilar | | |
| CS-064 | `dynamic` e `ExpandoObject` | | |
| CS-065 | Source generator simples (gerar `ToString`) | | |

### Biblioteca e ecossistema

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| CS-066 | `System.Text.Json`: serializar records, `JsonPropertyName` e conversor customizado | | |
| CS-067 | `File`, `Path`, `Directory`, `StreamReader` e `FileSystemWatcher` | | |
| CS-068 | `HttpClient` e `IHttpClientFactory`: GET e POST | | |
| CS-069 | `Regex`: grupos nomeados e `GeneratedRegex` | | |
| CS-070 | Injeção de dependência com `ServiceCollection`: Transient, Scoped e Singleton | | |
| CS-071 | `appsettings.json` + variáveis de ambiente + `IOptions<T>` | | |
| CS-072 | `ILogger` com logging estruturado | | |
| CS-073 | Minimal API: CRUD em memória com Swagger | | |
| CS-074 | CLI com subcomandos e saída colorida usando `System.CommandLine` ou `Spectre.Console` | | |
| CS-075 | Entity Framework Core: modelos, migrations, SQLite e LINQ virando SQL | | |
| CS-076 | xUnit: `[Theory]`, `[InlineData]` e mocks com Moq ou NSubstitute | | |
| CS-077 | NuGet: criar uma biblioteca de classes e um pacote local | | |
| CS-078 | Solução com vários projetos (console + biblioteca + testes) | | |
| CS-079 | Blazor, WinForms, WPF ou MAUI: app simples (contador ou lista de tarefas) | | |
| CS-080 | Native AOT / `dotnet publish` self-contained: comparar tamanhos e tempo de inicialização | | |

## 🔷 TypeScript

_Foco: sistema de tipos (uniões, genéricos, mapped/conditional types), narrowing, configuração do compilador, `.d.ts`, validação em runtime e ecossistema._

### Configuração e fundamentos

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| TS-001 | `tsc --init` e `strict`: entender cada flag; rodar com `tsx`/`ts-node` | | |
| TS-002 | Inferência: quando anotar e quando deixar inferir; `const` vs. `let` (tipos literais) | | |
| TS-003 | `any` vs. `unknown` vs. `never`: função com `unknown` e narrowing; função exaustiva com `never` | | |
| TS-004 | Arrays, tuplas e `readonly`: diferenças | | |
| TS-005 | `readonly` profundo: diferença entre `Readonly<T>`, `ReadonlyArray<T>` e `as const` em objetos aninhados | | |
| TS-006 | `enum` vs. `const enum` vs. união de literais vs. objeto `as const`: comparar o JS gerado | | |
| TS-007 | `as const` e `satisfies`: configuração tipada sem perder os literais | | |
| TS-008 | Opcionais, `undefined` vs. ausente e `exactOptionalPropertyTypes` | | |
| TS-009 | Index signatures e `Record<K, V>`; `noUncheckedIndexedAccess` | | |
| TS-010 | Compilar para ES5 e para ES2022 e comparar o JS gerado de `class`, `async` e `?.` | | |

### Narrowing e uniões

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| TS-011 | Union types e narrowing: `typeof`, `in`, `instanceof`, igualdade e truthiness | | |
| TS-012 | Type guards (`x is T`) e assertion functions (`asserts x is T`) | | |
| TS-013 | Discriminated unions: modelar `Forma` (círculo, retângulo) e calcular a área com `switch` exaustivo | | |
| TS-014 | Modelar o estado de uma requisição (`loading`, `success`, `error`) sem estados impossíveis | | |
| TS-015 | Interface vs. `type`: diferenças (merge de declarações, `extends` vs. `&`) | | |
| TS-016 | Intersection types e conflitos de propriedades | | |
| TS-017 | `strictNullChecks`: tratar `null`/`undefined`; `?.`, `??` e `!` (e por que `!` é perigoso) | | |
| TS-018 | `filter(Boolean)` não estreita o tipo: tipar corretamente com um type guard | | |
| TS-019 | Tipagem estrutural vs. nominal: mostrar quando dois tipos "diferentes" se misturam | | |
| TS-020 | Branded types: `UserId` e `OrderId` não intercambiáveis | | |
| TS-021 | `unique symbol`: usar símbolos como chaves tipadas e marcas de tipo | | |

### Funções, classes e genéricos

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| TS-022 | Overloads, parâmetros opcionais, rest tipado e `this` tipado | | |
| TS-023 | Reescrever uma função com 3 overloads usando um tipo condicional e comparar a ergonomia | | |
| TS-024 | Tipar `map`, `filter` e `reduce` caseiros | | |
| TS-025 | Genéricos: `identity<T>`, `primeiro<T>(arr: T[])`, restrições com `extends` e valores padrão | | |
| TS-026 | Inferência de genéricos: quando precisa de `NoInfer` ou de uma assinatura auxiliar | | |
| TS-027 | `pegar<T, K extends keyof T>(obj: T, key: K)` | | |
| TS-028 | Classes: `public`/`private`/`protected`/`readonly`, `#privado`, parameter properties, `abstract` e `implements` | | |
| TS-029 | `this` polimórfico e builder fluente tipado | | |
| TS-030 | Assinaturas de construtor (`new (...args) => T`): fábrica genérica e mixins tipados | | |
| TS-031 | `abstract class` + construtor `protected` + fábrica tipada | | |
| TS-032 | Variância: covariância e contravariância de parâmetros (`strictFunctionTypes`) | | |

### Tipos avançados

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| TS-033 | Utility types: `Partial`, `Required`, `Readonly`, `Pick`, `Omit`, `Record`, `Exclude`, `Extract`, `NonNullable`, `ReturnType`, `Parameters`, `Awaited`; um uso real para cada | | |
| TS-034 | Mapped types: `Mutavel<T>`, `Opcional<T>` e `Getters<T>` (com `as` e remapeamento de chaves) | | |
| TS-035 | Conditional types: `ElementType<T>`, `Flatten<T>` e `IsString<T>` | | |
| TS-036 | `infer`: extrair o tipo de retorno, de argumentos e de elementos de Promise | | |
| TS-037 | `Parameters` e `ReturnType` em funções sobrecarregadas: o que acontece e como contornar | | |
| TS-038 | Template literal types: tipo para rotas que começam com `/` e para nomes de evento como `onClick` | | |
| TS-039 | Tipos `CamelCase<S>` e `SnakeCase<S>` usando template literal types | | |
| TS-040 | Tipos recursivos: `DeepPartial`, `DeepReadonly` e o tipo `Json` | | |
| TS-041 | Tipos distributivos vs. não distributivos (`[T] extends [U]`) | | |
| TS-042 | `Omit` em uniões: por que não distribui e como criar um `DistributiveOmit` | | |
| TS-043 | Tipo `Paths<T>` que gera `"a.b.c"` a partir de um objeto aninhado | | |
| TS-044 | `keyof typeof obj` e `(typeof arr)[number]`: derivar tipos a partir de valores | | |
| TS-045 | Resolver pelo menos 10 desafios de nível fácil do repositório type-challenges | | |

### Aplicando os tipos

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| TS-046 | Tipar um `EventEmitter` fortemente (nome do evento determina o payload) | | |
| TS-047 | Tipar `pick`, `omit`, `groupBy` e `debounce` sem usar `any` | | |
| TS-048 | Tipar `Object.keys`/`Object.entries` corretamente (por que `keyof` não é retornado) e criar versões tipadas | | |
| TS-049 | Tipar `curry` e `pipe` com genéricos | | |
| TS-050 | Tipar `zip` e `unzip` com tuplas variádicas (variadic tuple types) | | |
| TS-051 | Máquina de estados em que transições inválidas não compilam | | |
| TS-052 | Store estilo Redux tipado: ações discriminadas e reducer exaustivo | | |
| TS-053 | Cliente de API tipado a partir de um objeto de rotas | | |
| TS-054 | `Result<T, E>` (como em Rust) em vez de `throw` | | |
| TS-055 | `catch (e)`: `unknown` e narrowing do erro; classes de erro customizadas e `instanceof` | | |
| TS-056 | Cache genérico com `Map<K, V>` | | |
| TS-057 | `Generator<Y, R, N>` e `AsyncIterable<T>` tipados | | |
| TS-058 | `Promise.all` com tuplas e `Awaited` | | |
| TS-059 | Tipar `retry<T>(fn: () => Promise<T>)` lidando com Promises aninhadas | | |

### Runtime vs. tipos

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| TS-060 | Os tipos não existem em execução: validar JSON com Zod ou Valibot e inferir o tipo (`z.infer`) | | |
| TS-061 | `JSON.parse` retorna `any`: criar `parse<T>(json, guarda)` segura | | |
| TS-062 | Tipos para DOM: `HTMLInputElement`, `querySelector<T>` e eventos tipados | | |
| TS-063 | Decorators (padrão TC39): de método (log), de classe e de propriedade | | |
| TS-064 | Servidor Express ou Fastify tipado (request/response) | | |
| TS-065 | React + TS: componente com props genéricas; `useState<T>` e `useReducer` com discriminated union | | |
| TS-066 | Wrapper tipado de `fetch` com genéricos e tratamento de erro | | |

### Módulos, declarações e ferramentas

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| TS-067 | `import type`, `export type` e `verbatimModuleSyntax`; ESM vs. CJS no `tsconfig` | | |
| TS-068 | `moduleResolution` (`node16`, `bundler`): provocar erros de import e entender cada um | | |
| TS-069 | `paths` e `baseUrl`: aliases como `@/` | | |
| TS-070 | Escrever um `.d.ts` para um módulo JS sem tipos; `declare module` e `declare global` | | |
| TS-071 | Publicar tipos: `declaration`, source maps e `exports`/`types` no `package.json` | | |
| TS-072 | Inspecionar o `.d.ts` que o `tsc --declaration` gera para a sua lib e simplificar os tipos inferidos | | |
| TS-073 | `@types/*` e DefinitelyTyped: instalar e entender | | |
| TS-074 | Namespaces e merge de declarações: quando ainda fazem sentido | | |
| TS-075 | ESLint com `typescript-eslint` (regras com tipo) e Prettier | | |
| TS-076 | Testes com Vitest ou Jest; testes de tipo (`expectTypeOf` ou `tsd`) | | |
| TS-077 | Monorepo com project references (`composite`) | | |
| TS-078 | `tsc --noEmit` no CI e o que `skipLibCheck` esconde | | |
| TS-079 | Migrar um arquivo JS de 100+ linhas para TS passo a passo (`allowJs`, `checkJs`, JSDoc) | | |
| TS-080 | Eliminar todos os `any` de um módulo e ligar a regra `no-explicit-any` | | |

## 🦀 Rust

_Foco: ownership, borrowing e lifetimes, enums e `match`, traits e genéricos, tratamento de erros, iteradores, ponteiros inteligentes, concorrência sem data races, macros e `unsafe`._

### Fundamentos

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| RS-001 | `cargo new`, `run`, `build`, `test`, `check`, `fmt` e `clippy`; debug vs. `--release` | | |
| RS-002 | Imutabilidade por padrão, `mut`, shadowing, constantes e `static` | | |
| RS-003 | Overflow: `wrapping_*`, `checked_*` e `saturating_*`; o que acontece em debug vs. release | | |
| RS-004 | Conversões: `as`, `From`/`Into`, `TryFrom` e `parse::<T>()` | | |
| RS-005 | `String` vs. `&str`; `char` e UTF-8; por que não se indexa uma string com número | | |
| RS-006 | Tuplas, arrays e slices (`&v[1..3]`) | | |
| RS-007 | Expressões vs. statements: `if`, `match` e blocos que retornam valor | | |
| RS-008 | `loop` com `break valor`, labels, `while let`, `for` com `.rev()` e `.step_by()` | | |

### Ownership, borrowing e lifetimes

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| RS-009 | Mover, clonar e copiar (`Copy`): prever quais linhas não compilam | | |
| RS-010 | `&` e `&mut`: as regras de empréstimo; provocar 5 erros do borrow checker e entender cada mensagem | | |
| RS-011 | Funções que recebem `&str`, `&[T]` e `&mut Vec<T>` evitando `clone` desnecessário | | |
| RS-012 | Lifetimes: `maior<'a>(a: &'a str, b: &'a str) -> &'a str` e uma struct que guarda `&str` | | |
| RS-013 | Elisão de lifetimes e `'static` | | |
| RS-014 | Retornar referência para variável local (erro) e corrigir de 3 formas | | |
| RS-015 | `mem::take`, `mem::replace` e `mem::swap` | | |
| RS-016 | `Cow<str>`: função que só aloca quando precisa modificar | | |

### Erros, `Option` e `Result`

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| RS-017 | `Option<T>`: `map`, `and_then`, `unwrap_or`, `?`, `if let` e `let else` | | |
| RS-018 | `Result<T, E>`: `?`, `map_err` e `ok_or`; ler um arquivo e converter o conteúdo em número | | |
| RS-019 | Erro customizado: `enum`, `impl Display`, `impl Error` e `From` para conversão automática; depois com `thiserror` e `anyhow` | | |
| RS-020 | `panic!`, `unwrap`, `expect` e `unreachable!`: quando é aceitável | | |
| RS-021 | `fn main() -> Result<(), Box<dyn Error>>` e códigos de saída do programa | | |
| RS-022 | `collect` em `Result<Vec<_>, _>`: falhar na primeira conversão que der erro | | |

### Tipos, enums e padrões

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| RS-023 | `struct` (nomeada, tupla e unit), `impl`, métodos, funções associadas e `Self` | | |
| RS-024 | `enum` com dados (`Mensagem::Move { x, y }`, `Write(String)`) e `match` exaustivo | | |
| RS-025 | `match` avançado: guardas, bindings com `@`, intervalos e desestruturação aninhada | | |
| RS-026 | Slice patterns: `[primeiro, .., ultimo]` e `[a, b, resto @ ..]` | | |
| RS-027 | Newtype pattern: `Metros(f64)` e `Segundos(f64)` não se misturam | | |
| RS-028 | Type-state pattern com `PhantomData`: `Porta<Aberta>` e `Porta<Fechada>` | | |
| RS-029 | Builder e `Default` com `..Default::default()` | | |
| RS-030 | Máquina de estados modelada com `enum` | | |

### Traits e genéricos

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| RS-031 | Definir e implementar um trait `Forma` com métodos padrão | | |
| RS-032 | Genéricos e trait bounds: `fn maior<T: PartialOrd>(...)`, `where` e `impl Trait` | | |
| RS-033 | Trait objects: `Box<dyn Trait>` vs. genéricos (despacho estático vs. dinâmico) e *object safety* | | |
| RS-034 | Traits da std: `Debug`, `Display`, `Clone`, `Copy`, `PartialEq`, `Eq`, `PartialOrd`, `Ord`, `Hash` e `Default`; `#[derive]` vs. manual | | |
| RS-035 | Operadores: `impl Add`, `Mul`, `Neg` e `Index` para `Vetor2D` ou `Matriz` | | |
| RS-036 | Regra do órfão (*orphan rule*): tentar implementar `Display` para `Vec<i32>` e contornar com newtype | | |
| RS-037 | `const fn` e `const generics`: `Matriz<const R: usize, const C: usize>` | | |
| RS-038 | `dyn Any` e downcast | | |
| RS-039 | Implementar `Ord` manualmente para uma struct em um `BinaryHeap` (Dijkstra) | | |

### Iteradores e closures

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| RS-040 | Implementar `Iterator` para `Fibonacci`; usar `map`, `filter`, `take`, `zip`, `enumerate`, `fold`, `flat_map`, `windows`, `chunks` e `peekable` | | |
| RS-041 | Adaptadores de iterador menos óbvios: `scan`, `chain`, `skip_while`, `take_while`, `min_by_key`, `max_by`, `rev` e `sum`; um problema para cada | | |
| RS-042 | `iter()` vs. `iter_mut()` vs. `into_iter()`: demonstrar a diferença de ownership | | |
| RS-043 | Closures: `Fn`, `FnMut` e `FnOnce`; `move`; retornar closures (`impl Fn` e `Box<dyn Fn>`) | | |
| RS-044 | Coleções: `Vec`, `VecDeque`, `HashMap` (API `entry`), `BTreeMap`, `HashSet` e `BinaryHeap`; um problema para cada | | |
| RS-045 | Ordenação: `sort`, `sort_by`, `sort_by_key`, `sort_unstable`; ordenar `f64` com `total_cmp` | | |

### Ponteiros inteligentes e memória

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| RS-046 | `Box<T>`: lista encadeada e árvore binária de busca | | |
| RS-047 | `Rc<T>` e `RefCell<T>`: árvore com ponteiro para o pai; `Weak` para evitar ciclos | | |
| RS-048 | Lista duplamente encadeada com `Rc<RefCell<...>>` e `Weak`; explicar por que é difícil em Rust | | |
| RS-049 | `Deref` e `Drop`: criar um tipo com `Drop` e observar a ordem de destruição (RAII) | | |
| RS-050 | `unsafe`: ponteiros brutos, `unsafe fn` e um wrapper seguro (ex.: seu próprio `split_at_mut`) | | |
| RS-051 | FFI: chamar uma função C a partir de Rust (`extern "C"`) e chamar Rust a partir de C | | |
| RS-052 | Reimplementar do zero um `Vec<T>` simplificado (com `unsafe` e alocador) | | |

### Concorrência

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| RS-053 | `thread::spawn`, `join` e `move`: somar um array em paralelo | | |
| RS-054 | Canais `mpsc`: produtor/consumidor | | |
| RS-055 | `Arc<Mutex<T>>`: contador compartilhado; `RwLock`; deadlock proposital | | |
| RS-056 | `Send` e `Sync`: tentar enviar um `Rc` para outra thread e entender o erro | | |
| RS-057 | `thread::scope`: usar referências locais dentro de threads | | |
| RS-058 | Atômicos: `AtomicUsize` e `Ordering` | | |
| RS-059 | `rayon`: trocar `iter()` por `par_iter()` e medir | | |
| RS-060 | `async/await` com `tokio`: `spawn`, `join!`, `select!`; HTTP com `reqwest` | | |
| RS-061 | `Future` e `Pin`: implementar manualmente um `Future` simples | | |
| RS-062 | `tokio::sync`: `mpsc`, `Mutex` e `Semaphore`; cancelamento | | |

### Macros, projeto e ecossistema

| ID | Desafio | Dev 1 | Dev 2 |
|:---:|---|:---:|:---:|
| RS-063 | Macros declarativas (`macro_rules!`): `meu_vec!`, `hashmap!` e `max!` | | |
| RS-064 | Usar e depois (avançado) escrever uma macro `derive` simples | | |
| RS-065 | Módulos: `mod`, `pub`, `use`, `pub(crate)` e arquivos separados | | |
| RS-066 | Workspace com uma crate de biblioteca e uma de binário | | |
| RS-067 | Crates populares: `rand`, `serde`, `serde_json`, `regex` e `chrono` | | |
| RS-068 | `clap`: CLI com subcomandos | | |
| RS-069 | `serde`: serializar e desserializar structs e enums (`rename`, `default`, `skip`) | | |
| RS-070 | Testes: `#[test]`, `#[should_panic]`, doc tests e testes de integração em `tests/` | | |
| RS-071 | Benchmark com `criterion`; perfil com `cargo flamegraph` | | |
| RS-072 | Documentação com `///` e exemplos executáveis; `cargo doc` | | |
| RS-073 | `std::fs` e `std::io`: `BufReader`, `lines()`, `Read` e `Write`; copiar arquivo | | |
| RS-074 | `std::env::args` e `std::process::exit` com códigos de saída | | |
| RS-075 | Servidor HTTP com `axum` ou `actix-web`: CRUD | | |
| RS-076 | Acesso a banco com `sqlx` ou `rusqlite` | | |
| RS-077 | Testes baseados em propriedades com `proptest` | | |
| RS-078 | Compilar uma função Rust para WebAssembly e chamá-la do JavaScript | | |
| RS-079 | Resolver pelo menos 20 exercícios do Rustlings | | |
| RS-080 | Reescrever em Rust um programa que você fez em C e comparar segurança e desempenho | | |

## 🔀 Desafios entre linguagens

_Para fazer em dupla, usando as linguagens de cada um._

| ID | Desafio | Feito |
|:---:|---|:---:|
| X-001 | Implementar o mesmo algoritmo (ex.: crivo de Eratóstenes até 10 milhões) em todas as linguagens do grupo e comparar tempo, memória e linhas de código | |
| X-002 | Escrever a mesma lista de tarefas de linha de comando (com persistência em JSON) em duas linguagens e comparar a experiência | |
| X-003 | Parser de JSON do zero em duas linguagens diferentes | |
| X-004 | Servidor TCP de eco em uma linguagem e o cliente em outra | |
| X-005 | Um programa grava dados em formato binário e o outro (em outra linguagem) lê, tratando endianness e padding | |
| X-006 | Um programa gera JSON e o outro (em outra linguagem) consome | |
| X-007 | Backend HTTP em uma linguagem e cliente/CLI em outra | |
| X-008 | Escrever uma biblioteca em C ou Rust e chamá-la de Python, de Node.js e de C# | |
| X-009 | Compilar uma função Rust ou C para WebAssembly e chamá-la do JavaScript/TypeScript | |
| X-010 | Montar uma tabela comparando como cada linguagem trata `null`, erros, strings, concorrência e gerenciamento de memória | |
| X-011 | Caça aos bugs: cada um escreve um programa com 5 bugs típicos da sua linguagem e o outro tenta achar (code review) | |
| X-012 | Portar a solução do colega de um desafio para a sua linguagem e comparar as duas | |
| X-013 | Duelo de otimização: otimizar ao máximo a mesma função (ex.: multiplicação de matrizes) em cada linguagem e comparar | |
| X-014 | Ler o código de um projeto open source pequeno na sua linguagem e abrir uma issue ou Pull Request | |
