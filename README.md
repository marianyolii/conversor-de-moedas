
# Conversor de Moedas

## 💎 Principais Funcionalidades

1. **updateCurrency** – Atualiza automaticamente o símbolo da moeda no campo de valor.
2. **Conversão de Moeda** – Realiza a conversão entre as moedas selecionadas.
3. **Exibição do Resultado** – Exibe o valor convertido em tempo real.

## 🚀 Características

1. **updateCurrency**: Detecta a moeda de origem escolhida e ajusta automaticamente o símbolo da moeda no campo de entrada, proporcionando uma interação mais fluida para o usuário.
   
2. **Conversão de Moeda**: Converte valores entre as moedas selecionadas (USD, EUR, BRL) com base nas taxas de câmbio atualizadas em tempo real. A API utilizada para essa operação é a [ExchangeRate API](https://app.exchangerate-api.com/dashboard).
   
3. **Validação de Entrada**: Garante que o valor inserido seja numérico, emitindo um alerta caso contrário, solicitando ao usuário que corrija antes de proceder com a conversão.

### 🟡 Resumo das Funcionalidades da API

Este projeto é uma versão aprimorada do [conversor de moeda simples](https://github.com/SarahLSilva/ConversorDeMoeda.git), permitindo que o usuário:

- Selecione a moeda de origem e a moeda de destino.
- Informe um valor e visualize o resultado da conversão em tempo real.
- Valide a entrada, garantindo que o valor seja numérico antes de realizar a conversão.

## 📑 Detalhamento do Código

1. **Constantes `apiKey` e `apiURL`**: Definem a chave da API e a URL base utilizadas para obter as taxas de câmbio mais recentes.

2. **Função `getExchangeRate`**: Utiliza `fetch` para buscar a taxa de câmbio entre as duas moedas selecionadas, acessando a API ExchangeRate. Em caso de erro, retorna `null` e exibe uma mensagem de erro no console.

3. **Função `updateCurrency`**: Ajusta o símbolo da moeda automaticamente no campo de entrada conforme a moeda escolhida. Também define um texto auxiliar (placeholder) para melhorar a experiência do usuário.

4. **Listener de Evento para Conversão**: O formulário escuta o evento `submit`. Quando disparado, ele coleta o valor e as moedas de origem e destino, consulta a taxa de câmbio via API, faz a conversão e apresenta o valor convertido.

### ✨ Características Distintivas no Código JavaScript

- **Validação Rigorosa**: O uso do operador de comparação estrita (`===`) garante precisão na comparação das moedas, evitando conversões automáticas de tipos.
- **updateCurrency()**: Atualiza automaticamente o símbolo e o texto de auxílio (placeholder) no campo de entrada, facilitando a identificação da moeda.
- **Tratamento de Erros**: Caso a busca pela taxa de câmbio falhe, uma mensagem amigável é exibida, sugerindo ao usuário tentar novamente.

## ⚙️ Instruções de Uso

1. Insira o valor a ser convertido no campo de entrada.
2. Selecione a moeda de origem no primeiro menu suspenso.
3. Escolha a moeda de destino no segundo menu suspenso.
4. Clique em "Converter" para visualizar o valor convertido.

## 🧮 Tecnologias Utilizadas
 
- **HTML** - Estrutura da interface.
- **CSS** - Estilização do layout e aparência.
- **JavaScript** - Lógica da aplicação, manipulação de DOM e integração com a API.
- **Chat GPT** - Apoio na criação de lógica e funções complexas.
 
## 📝 Fontes
 
- [Reverso](https://context.reverso.net/traducao/ingles-portugues/currency+symbol): Referência para símbolos de moeda.
- [Mozilla](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Strict_equality): Documentação sobre o operador de igualdade estrita.
- [ExchangeRate API](https://app.exchangerate-api.com/dashboard): API usada para obter as taxas de câmbio em tempo real.

 
## 👨‍🏫 Orientação
 
- [Professor Leonardo](https://github.com/leonardossrocha)

