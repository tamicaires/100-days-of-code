# Dia 4: DRY, KISS e YAGNI: O Que São, Para Que Servem e Exemplos

## **1. DRY (Don't Repeat Yourself)**  

### **O que é e para que serve?**  
O princípio DRY evita a repetição de código ao centralizar lógicas reutilizáveis em um único lugar. Isso torna o sistema mais organizado e fácil de manter, já que mudanças precisam ser feitas apenas uma vez.  

### **Exemplo**  
Imagine que você tem funções para calcular a área de um quadrado e de um retângulo. Em vez de criar duas funções separadas, centralizamos a lógica em uma única função.  

#### Antes (violando DRY):
```javascript
const calcularAreaQuadrado = (lado) => lado * lado;
const calcularAreaRetangulo = (largura, altura) => largura * altura;
```
#### Depois (aplicando DRY):
```javascript
const calcularArea = (forma, dimensoes) => {
  if (forma === "quadrado") return dimensoes.lado ** 2;
  if (forma === "retangulo") return dimensoes.largura * dimensoes.altura;
};
```

#### Uso:
```javascript
calcularArea("quadrado", { lado: 4 }); // Resultado: 16
calcularArea("retangulo", { largura: 5, altura: 3 }); // Resultado: 15
```

### Por que é melhor?
Agora temos apenas uma função para gerenciar. Se precisar de ajustes, fazemos em um único local.

## 2. KISS (Keep It Simple, Stupid)
### O que é e para que serve?
O princípio KISS enfatiza a simplicidade no código. Soluções simples são mais fáceis de entender, testar e manter. Complexidade desnecessária aumenta o risco de erros e dificulta o trabalho da equipe.

### Exemplo
Vamos criar uma função que realiza operações matemáticas básicas, como soma e subtração.

Antes (violando KISS):
```javascript
function calcular(num1, num2, operador) {
  if (operador === "+") return num1 + num2;
  else if (operador === "-") return num1 - num2;
  else if (operador === "*") return num1 * num2;
  else if (operador === "/") return num1 / num2;
  else throw new Error("Operador inválido");
}
```
### Depois (aplicando KISS):
```javascript
const calcular = (num1, num2, operador) => {
  const operacoes = {
    "+": num1 + num2,
    "-": num1 - num2,
    "*": num1 * num2,
    "/": num1 / num2,
  };
  return operacoes[operador] ?? "Operador inválido";
};
```

### Uso:
```javascript
calcular(10, 5, "+"); // Resultado: 15
calcular(10, 5, "%"); // Resultado: "Operador inválido"
```

### Por que é melhor?
A lógica está mais compacta e clara, reduzindo linhas de código e erros potenciais.

## 3. YAGNI (You Aren't Gonna Need It)
### O que é e para que serve?
O princípio YAGNI afirma que você não deve implementar funcionalidades a menos que sejam necessárias agora. Isso evita esforço desnecessário e mantém o código mais limpo e objetivo.

### Exemplo
Digamos que você queira aplicar desconto apenas para usuários premium. Não há necessidade de antecipar tipos adicionais de usuários.

### Antes (violando YAGNI):
```javascript
function aplicarDesconto(usuario, valor) {
  if (usuario.tipo === "premium" || usuario.tipo === "gold" || usuario.tipo === "platinum") {
    return valor * 0.9;
  }
  return valor;
}
```

### Depois (aplicando YAGNI):
```javascript
function aplicarDesconto(usuario, valor) {
  if (usuario.tipo === "premium") return valor * 0.9;
  return valor;
}
```

### Uso:
```javascript
aplicarDesconto({ tipo: "premium" }, 100); // Resultado: 90
aplicarDesconto({ tipo: "comum" }, 100);  // Resultado: 100
```

### Por que é melhor?
Implementamos apenas o necessário, economizando tempo e esforço. Podemos expandir para outros tipos de usuários se realmente for preciso no futuro.

### Em resumo:
DRY: Centralize lógicas reutilizáveis para evitar duplicações desnecessárias.
KISS: Prefira soluções simples e diretas, sem adicionar complexidade desnecessária.
YAGNI: Desenvolva apenas o que é necessário no momento, evitando trabalho e código inúteis.

Esses princípios ajudam a criar sistemas limpos, eficientes e fáceis de escalar. Seguindo-os, você reduz erros, facilita manutenções futuras e economiza tempo no desenvolvimento.
