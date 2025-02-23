# Capítulo 9 – Refactoring  

## 1. Introdução  
Refactoring refere-se a **modificações no código** que melhoram sua **legibilidade, organização e manutenibilidade**, sem alterar o funcionamento do sistema.  

A necessidade de refatoração surge devido à **evolução natural do software**. Segundo as **Leis de Lehman**, sistemas de software envelhecem com o tempo, tornando-se mais complexos e difíceis de manter. O **refactoring** combate esse envelhecimento ao melhorar a estrutura do código sem modificar sua funcionalidade.  

O conceito foi formalizado por **Martin Fowler** em 2000, com um catálogo de técnicas que ajudam a melhorar código existente. Ele enfatiza que refactoring deve ser feito **continuamente**, para evitar acúmulo de "dívida técnica".  

## 2. Principais Técnicas de Refactoring  

### 2.1 Extração de Método  
Separa trechos de código repetitivos ou longos em métodos menores e mais legíveis.  

**Exemplo Antes:**  
```java
void calcularSalario() {
  double imposto = salario * 0.2;
  double bonus = salario * 0.1;
  salario = salario - imposto + bonus;
}
```
**Após Refatoração:**  
```java
void calcularSalario() {
  double imposto = calcularImposto();
  double bonus = calcularBonus();
  salario = salario - imposto + bonus;
}

double calcularImposto() { return salario * 0.2; }
double calcularBonus() { return salario * 0.1; }
```

### 2.2 Inline de Método  
Remove métodos desnecessários e insere seu código diretamente no chamador.  

**Exemplo Antes:**  
```java
double calcularImposto() { return salario * 0.2; }
void calcularSalario() { salario = salario - calcularImposto(); }
```
**Após Refatoração:**  
```java
void calcularSalario() { salario = salario - (salario * 0.2); }
```

### 2.3 Movimentação de Método  
Transfere um método para outra classe quando ele acessa mais dados de outra classe do que da própria.  

**Exemplo Antes:**  
```java
class Cliente {
  Endereco endereco;
  String getCep() { return endereco.cep; }
}
```
**Após Refatoração:**  
```java
class Endereco {
  String cep;
  String getCep() { return cep; }
}
class Cliente {
  Endereco endereco;
}
```
