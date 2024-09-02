# GHLA.mq5 - Gann HiLo Activator Indicator

O **GHLA** (Gann HiLo Activator) é um indicador técnico customizado desenvolvido para a plataforma MetaTrader 5. Este indicador é utilizado para identificar tendências de mercado e pontos de ativação para operações de compra ou venda, com base na média dos preços altos e baixos de um período específico.

## Sobre o Indicador

- **Nome:** Gann HiLo Activator
- **Versão:** 1.00
- **Autor:** MetaQuotes Software Corp.
- **Licença:** Copyright 2018, MetaQuotes Software Corp.
- **Link:** [MetaQuotes](https://mql5.com)

## Descrição

O **Gann HiLo Activator** é um indicador que calcula a média móvel dos preços altos (HIGH) e baixos (LOW) para um determinado período. Ele utiliza essas médias móveis para identificar a direção da tendência atual do mercado. Quando o preço de fechamento está acima da média móvel de preços altos, o indicador sugere uma tendência de alta, e vice-versa.

### Parâmetros de Entrada

- **InpPeriod (Período):** Define o número de barras que serão utilizadas para calcular a média móvel. O valor padrão é 10.

### Buffers do Indicador

O indicador utiliza cinco buffers para armazenar os dados calculados:

1. **BufferGHLA:** Armazena os valores do Gann HiLo Activator.
2. **BufferColors:** Controla a cor da linha do indicador (verde para alta, vermelho para baixa, cinza escuro para neutro).
3. **BufferMAH:** Contém a média móvel dos preços altos.
4. **BufferMAL:** Contém a média móvel dos preços baixos.
5. **BufferDir:** Indica a direção atual da tendência.

## Como Funciona

1. **Inicialização:** Durante a inicialização (`OnInit`), o indicador configura os buffers e cria as médias móveis de acordo com o período especificado pelo usuário.
   
2. **Cálculo:** No método `OnCalculate`, o indicador calcula a média móvel de preços altos e baixos para o número de barras definido. Em seguida, ele compara o preço de fechamento com essas médias móveis para determinar a direção da tendência e ajustar o valor de `BufferGHLA` e `BufferColors` de acordo.

3. **Indicação de Tendência:**
   - **Alta:** Se o preço de fechamento estiver acima da média móvel dos preços altos (`MAH`), o indicador mostra uma linha verde.
   - **Baixa:** Se o preço de fechamento estiver abaixo da média móvel dos preços baixos (`MAL`), o indicador mostra uma linha vermelha.
   - **Neutro:** Se o preço de fechamento estiver entre as médias móveis, o indicador permanece neutro.

## Exemplo de Uso

Para utilizar o indicador **GHLA** no MetaTrader 5:

1. Adicione o arquivo `GHLA.mq5` à pasta de indicadores no diretório do MetaTrader 5.
2. Compile o indicador usando o MetaEditor.
3. Adicione o indicador ao seu gráfico para começar a monitorar as tendências do mercado.

## Requisitos

- **Plataforma:** MetaTrader 5
- **Linguagem:** MQL5

## Contribuição

Contribuições para melhorar o **GHLA** são bem-vindas! Sinta-se à vontade para abrir uma *issue* ou enviar um *pull request* com suas melhorias.

## Contato

Para mais informações ou suporte, visite [MetaQuotes](https://mql5.com).
