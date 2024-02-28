Funções, assinatura, parâmetros e retorno
=========================================

Segue código

```js
// assinatura da função (do método)
// keyword nomeDaFuncao(param1, param2, param...)
function abs(n) { return n < 0 ? n * -1 : n }
// paypal
function pow(base, exp) {
  if (exp % 1 != 0) { // é decimal
    throw 'expoente decimal não suportado'
  }
  if (typeof(base) != 'number' || typeof(exp) != 'number') {
    return NaN
  }
  // caso especial
  if (exp == 0) return 1
  // var -> escopo de função
  var res = base
  for (var i = 1; i < abs(exp); i++) res *= base
  // if (exp < 0) return 1 / res
  // else return res
  return exp < 0 ? 1 / res : res // expressão ternária
}

console.log(abs(-2))
console.log(abs(2))
console.log(abs(0))
console.log(abs(-0))
console.log(abs(Infinity))

console.log(pow(2, 5))
// console.log(pow(3, 4.5))
console.log(pow(2, -8))

console.log(pow(4, 5.8))
// console.log(typeof(3))
console.log(pow(5, 0)) // 1
console.log(pow(2, 5))
console.log(pow(-2, 4))
console.log(pow(2, -4))
console.log(pow(2, 2.5))
console.log(Math.pow(2, 2.5))
//console.log(pow(2, 5) == 32)
//console.log(pow(2, 10)) // 1024
// casos especiais (edge case, corner case)

// bitwise op: js tornar number um int32



// chamar função (function call)
// invocar função (invoke a function)

/*
b1 = 2
e1 = 8

console.log(Math.pow(b1, e1))
console.log(b1 ** e1) // chama o Math.pow
console.log(Math.pow(3, 9))

res = b1
// lógica calcular a potência b1 ^ e1
for (var i = 1; i < e1; i++) res *= b1

console.log(res) // 256

b2 = 5
e2 = 3

res = b2
for (var i = 1; i < e2; i++) res *= b2
console.log(res) // 125

*/
```
