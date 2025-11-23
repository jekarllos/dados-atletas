# dados-atletas

Um sistema em JavaScript para gerenciar dados de atletas, calculando categoria, IMC e média de desempenho.

## 📋 Descrição

O projeto `dados-atletas` implementa uma classe `Atleta` que concentra informações de um atleta e fornece métodos para calcular parâmetros importantes como categoria de competição, índice de massa corporal (IMC) e média válida de notas.

## 🚀 Funcionalidades

- **Categorização automática** de atletas por faixa etária
- **Cálculo de IMC** para avaliação física
- **Cálculo de média válida** ignorando notas inválidas
- **Getters** para acesso seguro aos dados do atleta

## 📦 Instalação

1. Clone o repositório:
```bash
git clone https://github.com/jekarllos/dados-atletas/dados-atletas.git
cd dados-atletas
```

2. Importe o arquivo em seu projeto JavaScript:
```javascript
// No Node.js
const Atleta = require('./dados-atletas.js');

// Ou em um arquivo HTML
<script src="dados-atletas.js"></script>
```

## 💻 Como Usar

### Criar um atleta
```javascript
const atleta = new Atleta("Cesar Abascal", 30, 80, 1.70, [10, 9.34, 8.42, 10, 7.88]);
```

### Acessar informações
```javascript
console.log(atleta.obtemNomeAtleta());      // "Cesar Abascal"
console.log(atleta.obtemIdadeAtleta());     // 30
console.log(atleta.obtemPesoAtleta());      // 80
console.log(atleta.obtemNotasAtleta());     // [10, 9.34, 8.42, 10, 7.88]
```

### Obter cálculos
```javascript
console.log(atleta.obtemCategoria());       // "Adulto"
console.log(atleta.obtemIMC());             // 27.68166089965398
console.log(atleta.obtemMediaValida());     // 9.128
```

## 📊 Categorias de Atletas

| Categoria | Idade |
|-----------|-------|
| Infantil | 9 a 11 anos |
| Juvenil | 12 a 13 anos |
| Intermediário | 14 a 15 anos |
| Adulto | 16 a 30 anos |
| Sem categoria | Outras idades |

## 📐 Cálculos Implementados

### IMC (Índice de Massa Corporal)
```
IMC = peso / (altura × altura)
```

### Média Válida
Calcula a média aritmética das notas, ignorando valores inválidos (NaN ou null).

## 🏗️ Estrutura da Classe

### Propriedades
- `nome` (string) - Nome do atleta
- `idade` (number) - Idade em anos
- `peso` (number) - Peso em kg
- `altura` (number) - Altura em metros
- `notas` (array) - Array de notas/scores

### Métodos

**Cálculos:**
- `calculaCategoria()` - Retorna a categoria do atleta
- `calculaIMC()` - Retorna o IMC calculado
- `calculaMediaValida()` - Retorna a média válida das notas

**Getters:**
- `obtemNomeAtleta()` - Retorna o nome
- `obtemIdadeAtleta()` - Retorna a idade
- `obtemPesoAtleta()` - Retorna o peso
- `obtemNotasAtleta()` - Retorna as notas
- `obtemCategoria()` - Retorna a categoria
- `obtemIMC()` - Retorna o IMC
- `obtemMediaValida()` - Retorna a média válida

## 📝 Exemplo Completo

```javascript
// Criar um atleta
const atleta = new Atleta("Cesar Abascal", 30, 80, 1.70, [10, 9.34, 8.42, 10, 7.88]);

// Exibir informações
console.log(`Nome: ${atleta.obtemNomeAtleta()}`);
console.log(`Idade: ${atleta.obtemIdadeAtleta()}`);
console.log(`Peso: ${atleta.obtemPesoAtleta()}`);
console.log(`Altura: ${atleta.obtemPesoAtleta()}`);
console.log(`Notas: ${atleta.obtemNotasAtleta()}`);
console.log(`Categoria: ${atleta.obtemCategoria()}`);
console.log(`IMC: ${atleta.obtemIMC()}`);
console.log(`Média válida: ${atleta.obtemMediaValida()}`);

// Saída:
// Nome: Cesar Abascal
// Idade: 30
// Peso: 80
// Altura: 1.7
// Notas: 10,9.34,8.42,10,7.88
// Categoria: Adulto
// IMC: 27.68166089965398
// Média válida: 9.128
```

## 🔧 Requisitos

- JavaScript ES6 ou superior
- Node.js (opcional, para execução em servidor)

## 📄 Licença

Este projeto é fornecido como material educacional.

## 👤 Autor

Desenvolvido como projeto de certificação JavaScript.

---

**Dica:** Para testar o projeto, abra o console do navegador ou use Node.js e execute os exemplos acima!
