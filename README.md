# JEST Unit Tests

## GitHub Actions

[![Build and Tests](https://github.com/taylorteixeira/prova01-unit-test-taylor/actions/workflows/node.js.yml/badge.svg?branch=main)](https://github.com/taylorteixeira/prova01-unit-test-taylor/actions/workflows/node.js.yml)

## SonarCloud

[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=taylorteixeira_prova01-unit-test-taylor&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=taylorteixeira_prova01-unit-test-taylor)

Este projeto contém uma implementação de testes unitários usando Jest para uma classe utilitária JavaScript com diversos métodos para manipulação de strings, operações matemáticas, manipulação de arrays e objetos.

## 📋 Índice

- [Sobre o Projeto](#sobre-o-projeto)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Instalação](#instalação)
- [Como Executar os Testes](#como-executar-os-testes)
- [Funcionalidades Testadas](#funcionalidades-testadas)
- [Metodologia de Teste](#metodologia-de-teste)
- [Cobertura de Testes](#cobertura-de-testes)
- [Exemplos de Uso](#exemplos-de-uso)

## 🎯 Sobre o Projeto

Este projeto foi desenvolvido como uma prova de conceito para demonstrar a implementação de testes unitários abrangentes usando o framework Jest. A classe `Utilitarios` oferece 25 métodos diferentes que cobrem as principais operações de manipulação de dados em JavaScript.

## 🚀 Tecnologias Utilizadas

- **JavaScript (ES6+)**: Linguagem de programação
- **Node.js**: Ambiente de execução
- **Jest**: Framework de testes
- **NPM**: Gerenciador de pacotes

## 📁 Estrutura do Projeto

```
prova01-unit-test-taylor/
├── src/
│   └── utilitarios.js          # Classe principal com métodos utilitários
├── test/
│   └── utilitarios.test.js     # Arquivo de testes
├── package.json                # Configurações do projeto
└── README.md                   # Este arquivo
```

## ⚙️ Instalação

1. **Clone o repositório:**
```bash
git clone https://github.com/seu-usuario/prova01-unit-test-taylor.git
cd prova01-unit-test-taylor
```

2. **Instale as dependências:**
```bash
npm install
```

## 🧪 Como Executar os Testes

### Executar todos os testes
```bash
npm test
```

### Executar com relatório de cobertura
```bash
npm test -- --coverage
```

### Executar em modo watch (observa mudanças)
```bash
npm test -- --watch
```

### Executar teste específico
```bash
npm test utilitarios.test.js
```

### Executar testes com detalhes verbosos
```bash
npm test -- --verbose
```

## 🔧 Funcionalidades Testadas

### 📝 Métodos de String (9 métodos)
- `inverterString()` - Inverte uma string
- `contarCaracteres()` - Conta caracteres de uma string
- `paraMaiusculas()` - Converte para maiúsculas
- `paraMinusculas()` - Converte para minúsculas
- `primeiraLetraMaiuscula()` - Primeira letra maiúscula
- `removerEspacos()` - Remove espaços das extremidades
- `repetirTexto()` - Repete texto N vezes
- `contarPalavras()` - Conta palavras em uma string
- `ehPalindromo()` - Verifica se é palíndromo

### 🧮 Métodos Matemáticos (8 métodos)
- `somar()` - Soma dois números
- `subtrair()` - Subtrai dois números
- `multiplicar()` - Multiplica dois números
- `dividir()` - Divide dois números (com tratamento de erro)
- `ehPar()` - Verifica se número é par
- `ehNumero()` - Verifica se valor é número
- `gerarNumeroAleatorio()` - Gera número aleatório
- `mediaArray()` - Calcula média de array

### 📊 Métodos de Array (8 métodos)
- `primeiroElemento()` - Retorna primeiro elemento
- `ultimoElemento()` - Retorna último elemento
- `tamanhoArray()` - Retorna tamanho do array
- `ordenarArray()` - Ordena array
- `inverterArray()` - Inverte array
- `juntarArray()` - Junta elementos com separador
- `removerDuplicados()` - Remove elementos duplicados

### 🏗️ Métodos de Objeto (2 métodos)
- `mesclarObjetos()` - Mescla dois objetos

## 🎯 Metodologia de Teste

### Padrão AAA (Arrange, Act, Assert)
```javascript
test("Deve somar dois números corretamente", () => {
  // Arrange - Preparar dados
  const a = 5, b = 3;
  
  // Act - Executar ação
  const resultado = utilitarios.somar(a, b);
  
  // Assert - Verificar resultado
  expect(resultado).toBe(8);
});
```

### Tipos de Teste Implementados

#### ✅ **Testes de Caso Normal**
```javascript
expect(utilitarios.paraMaiusculas("hello")).toBe("HELLO");
```

#### 🔍 **Testes de Caso Limite**
```javascript
expect(utilitarios.contarCaracteres("")).toBe(0);
expect(utilitarios.mediaArray([])).toBe(0);
```

#### ❌ **Testes de Caso de Erro**
```javascript
expect(() => utilitarios.dividir(10, 0)).toThrow("Divisão por zero");
```

#### 🎲 **Testes de Comportamento**
```javascript
test("Deve gerar número aleatório dentro do limite", () => {
  const numero = utilitarios.gerarNumeroAleatorio(10);
  expect(numero).toBeGreaterThanOrEqual(0);
  expect(numero).toBeLessThan(10);
});
```

### Matchers Utilizados
- `toBe()` - Comparação exata
- `toEqual()` - Comparação profunda (objetos/arrays)
- `toThrow()` - Verifica se lança exceção
- `toBeGreaterThanOrEqual()` - Maior ou igual
- `toBeLessThan()` - Menor que



## 👨‍💻 Autor

**Taylor** - Desenvolvedor do projeto

---

*Este projeto demonstra as melhores práticas em testes unitários com Jest, fornecendo uma base sólida para desenvolvimento orientado
