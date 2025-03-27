<!-- LTeX: language=pt-br -->
# Compiladores, na Prática

## Geração de código

### Variáveis locais

Variáveis locais podem ser representadas de várias formas, dependendo de seu tipo
e como são utilizadas.

- Podem ser otimizados diretamente como registradores.

```c
int x = 0;
int y = 1 + 2;
```

- `x` não pode ser usado como registrador, pois seu endereço é tomado.

```c
int  x = 0;
int *y = &x;
```

## Nossa estratégia

Não é permitido tomar o endereço de uma variável declarada com `var`. Para
se ter uma referência sera preciso usar um alocador local `alloca`.

```js
var x = alloca(0); // *int
```

> Vamos ignorar o stack por enquanto

## Adições na AST

## Codegen

Como estamos analisando o código enquanto realizamos codegen, é agora que
definiremos regras de escopo.
