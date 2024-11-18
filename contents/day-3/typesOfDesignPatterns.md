# Dia 3: Design Patterns: O que são, Quando Usar e Como Usar

## O que são Design Patterns? 🤔

**Design Patterns** (Padrões de Projeto) são soluções reutilizáveis para problemas comuns que surgem no desenvolvimento de software. Eles representam práticas consagradas para organizar o código de forma eficiente, modular e fácil de manter. Em vez de reinventar a roda toda vez que você enfrentar um problema, os Design Patterns oferecem soluções comprovadas que funcionam bem em uma variedade de contextos.

## Categorias dos Design Patterns 📚

Existem três principais categorias de Design Patterns:

1. **Criacionais** 🛠️
2. **Estruturais** 🔧
3. **Comportamentais** 🧠

Abaixo, vamos detalhar o que são, quando usar e como usar os padrões de cada categoria.

---

## 1. Padrões Criacionais 🛠️

### O que são? 🤷‍♂️
Os **Padrões Criacionais** tratam de como **criar objetos** de maneira eficiente, flexível e controlada. Eles ajudam a abstrair a criação de objetos, desacoplando o código que os utiliza da maneira como são instanciados.

### Quando Usar? 📅
Use padrões criacionais quando a criação de objetos for complexa ou variável, ou quando você precisa garantir que a criação de instâncias de um objeto seja controlada e flexível.

### Como Usar? 📝
- **Singleton**: Use quando você precisar garantir que uma classe tenha **somente uma instância** e oferecer um ponto global de acesso.
- **Factory Method**: Use quando você quiser definir uma interface para criar objetos, mas deixar a decisão da classe concreta para as subclasses.
- **Abstract Factory**: Use quando você precisar criar **famílias de objetos** relacionados sem especificar suas classes concretas.
- **Builder**: Use quando a construção de um objeto seja **complexa** e você quiser separar a construção da sua representação final.
- **Prototype**: Use quando criar novos objetos for **custoso** e você quiser clonar ou copiar um objeto existente.

---

## 2. Padrões Estruturais 🔧

### O que são? 🛠️
Os **Padrões Estruturais** lidam com a **organização e composição** de classes e objetos, facilitando a criação de sistemas complexos sem gerar um código rígido ou excessivamente acoplado.

### Quando Usar? 📅
Use padrões estruturais quando precisar **organizar** a forma como diferentes classes e objetos interagem entre si, de maneira que o sistema seja modular e flexível.

### Como Usar? 📝
- **Adapter**: Use quando precisar fazer com que classes com **interfaces incompatíveis** trabalhem juntas, convertendo uma interface em outra que o cliente espera.
- **Decorator**: Use quando quiser adicionar funcionalidades extras a um objeto de forma dinâmica, sem alterar sua classe original.
- **Facade**: Use quando quiser oferecer uma **interface simplificada** para um subsistema complexo, escondendo a complexidade interna.
- **Composite**: Use quando tiver uma **hierarquia** de objetos e precisar tratá-los de maneira uniforme, como se fosse um único objeto.
- **Proxy**: Use quando precisar controlar o acesso a um objeto, como por exemplo, para implementar **lazy loading**, **cache** ou **controle de segurança**.

---

## 3. Padrões Comportamentais 🧠

### O que são? 💡
Os **Padrões Comportamentais** se concentram em como os **objetos interagem entre si** e como a responsabilidade é distribuída de forma eficiente, evitando acoplamentos desnecessários e aumentando a flexibilidade do código.

### Quando Usar? 📅
Use padrões comportamentais quando precisar controlar a **comunicação** entre objetos ou distribuir responsabilidades de forma mais eficiente, para que o código seja mais flexível e fácil de entender.

### Como Usar? 📝
- **Observer**: Use quando quiser que um objeto **notifique automaticamente** outros objetos interessados sempre que seu estado mudar.
- **Strategy**: Use quando precisar de uma **família de algoritmos** intercambiáveis, permitindo que o algoritmo usado seja alterado sem modificar o código que o utiliza.
- **Command**: Use quando quiser **encapsular solicitações** como objetos, permitindo que comandos sejam tratados de forma flexível (ex: desfazer/refazer operações).
- **State**: Use quando o comportamento de um objeto mudar de acordo com seu **estado interno**, sem precisar de muitas condicionais.
- **Template Method**: Use quando quiser definir a estrutura geral de um algoritmo e deixar que as subclasses implementem partes específicas do algoritmo.
- **Chain of Responsibility**: Use quando precisar que **múltiplos objetos** tratem uma solicitação, passando-a ao longo de uma **cadeia** até que alguém consiga processá-la.
- **Memento**: Use quando precisar **salvar e restaurar** o estado interno de um objeto sem violar o princípio de encapsulamento.
- **Interpreter**: Use quando precisar **interpretar expressões** em um idioma específico e tiver uma gramática definida que pode ser modelada por objetos.
- **Iterator**: Use quando precisar acessar os elementos de uma **coleção de objetos** sequencialmente, sem expor sua estrutura interna.
- **Mediator**: Use quando quiser centralizar a **comunicação** entre objetos, evitando que eles se comuniquem diretamente uns com os outros.
- **Visitor**: Use quando quiser adicionar **novas operações** a objetos de uma estrutura sem alterar as classes desses objetos.

---

## Resumo: Quando e Como Usar Design Patterns

### **Quando Usar?** 📅
- Quando seu código começar a ficar **complexo** ou difícil de manter.
- Quando você precisar de **flexibilidade** e **escabilidade** no sistema.
- Quando você identificar um **problema comum de design** que pode ser resolvido com uma solução consagrada.

### **Como Usar?** 📝
1. **Identifique o Problema**: Antes de aplicar qualquer padrão, analise o problema que você está tentando resolver.
2. **Escolha o Padrão Adequado**: Baseado na sua análise, escolha o padrão que melhor se adapta à situação. Não force um padrão onde ele não se encaixa!
3. **Implemente o Padrão**: Aplique o padrão no seu código, mantendo a simplicidade e clareza. Lembre-se, a intenção dos Design Patterns é simplificar, não complicar.
4. **Refatore e Teste**: Após aplicar o padrão, refatore o código para garantir que ele se mantém **limpo**, **modular** e fácil de entender. Teste também para garantir que a mudança não introduziu novos problemas.

---

## Conclusão 🎯

**Design Patterns** são ferramentas poderosas para organizar, simplificar e melhorar a qualidade do código. Quando usados corretamente, eles ajudam a construir sistemas mais **flexíveis**, **modulares** e **fáceis de manter**, economizando tempo e esforço a longo prazo. Ao aprender a escolher o padrão certo para o problema certo, você estará no caminho para criar software mais robusto e escalável.
