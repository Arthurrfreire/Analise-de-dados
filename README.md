## Análise de Cancelamentos de Clientes com Python

Este projeto utiliza Python e a biblioteca Pandas para analisar um conjunto de dados de cancelamento de clientes, com o objetivo de entender os principais motivos de cancelamento e identificar ações para reduzir esse número.

## Contexto
Uma empresa com mais de 800 mil clientes percebeu que a maioria deles está inativa, ou seja, já cancelaram o serviço. Para melhorar seus resultados, a empresa deseja entender os principais fatores que levam ao cancelamento e encontrar maneiras de reduzir essa taxa.

## Estrutura do Projeto

* `cancelamentos.csv:` Arquivo de dados contendo informações sobre os clientes e seus cancelamentos.
* `README.md:` Este arquivo de documentação.
* `analise.ipynb:` Notebook Jupyter com o código Python para a análise.

## Dependências

Certifique-se de ter as seguintes bibliotecas Python instaladas:

* `pandas`
* `plotly`

## Processo de Análise

1. **Carregamento e Limpeza dos Dados:**
   
   * O arquivo `cancelamentos.csv` é lido em um DataFrame Pandas.
   
   * A coluna `CustomerID` é removida, pois não é relevante para a análise.
   
   * Valores ausentes são removidos do DataFrame.
   

3. **Análise Exploratória:**
   
   * Calcula-se a proporção de clientes que cancelaram e que não cancelaram o serviço.
   
   * Analisa-se a distribuição da duração do contrato e a taxa de cancelamento por tipo de contrato.
   
   * Remove-se a categoria "Monthly" (contrato mensal) da análise, pois apresenta uma taxa de cancelamento muito alta.
   
   * Analisa-se a distribuição do tipo de assinatura e a taxa de cancelamento por tipo de assinatura.
   

5. **Visualização de Dados:**
   
   * Histogramas são gerados para cada coluna, com cores diferentes para clientes que cancelaram e que não cancelaram.
   
   * A partir dos histogramas, identificam-se duas variáveis importantes: `ligacoes_callcenter` e `dias_atraso`.
   
7. **Refinamento da Análise:**
   
   * Removem-se os clientes com mais de 5 ligações para o call center e com mais de 20 dias de atraso.
   
   * Recalcula-se a taxa de cancelamento, que agora é de 18%.

## Conclusões

A análise identificou três fatores principais que contribuem para o cancelamento de clientes:

  * Contratos mensais
   
  * Necessidade de ligações frequentes para o call center
  
  * Atraso nos pagamentos

## Próximos Passos

Com base nessas descobertas, a empresa pode tomar medidas para reduzir a taxa de cancelamento, como:

  * Oferecer planos de contrato mais longos com benefícios adicionais.
    
  * Melhorar o atendimento ao cliente para reduzir a necessidade de ligações para o call center.
    
  * Implementar estratégias para reduzir o atraso nos pagamentos, como lembretes e incentivos.
    

**Importante:** Esta análise é um ponto de partida. É recomendado aprofundar a investigação, explorando outras variáveis e utilizando técnicas mais avançadas, como modelos de aprendizado de máquina, para prever o churn e identificar outras oportunidades de melhoria.
