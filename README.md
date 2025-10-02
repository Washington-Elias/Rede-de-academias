# Rede de Academias 🏋️‍♀️💪

## Descrição do Projeto
Este projeto analisa dados de clientes de uma rede de academias para identificar fatores relacionados à **rotatividade (churn)**.  
Foram aplicadas técnicas de estatística, machine learning e clusterização para prever e compreender os principais motivos que levam clientes a cancelar seus planos, além de propor **ações de retenção**.

## Ferramentas e Bibliotecas Utilizadas
- **Pandas** – manipulação de dados  
- **Matplotlib & Seaborn** – visualizações gráficas  
- **Scikit-learn** – modelos de machine learning (Regressão Logística, Random Forest, K-Means, StandardScaler)  
- **Scipy** – análise de agrupamentos hierárquicos (dendrograma)  

## Tabela
O dataset `gym_churn_us.csv` contém:
- **Idade (Age)** – idade do cliente  
- **Lifetime** – tempo total de relacionamento com a academia (em meses)  
- **Avg_additional_charges_total** – média de gastos adicionais  
- **Avg_class_frequency_total** – frequência média em aulas durante toda a assinatura  
- **Avg_class_frequency_current_month** – frequência em aulas no último mês  
- **Contract_period** – duração do contrato (mensal, trimestral, anual)  
- **Group_visits** – se participa de visitas/aulas em grupo  
- **Promo_friends** – se entrou por indicação de amigos  
- **Churn** – variável alvo (1 = cancelou, 0 = permaneceu)  

## Metodologia
1. **Exploração inicial dos dados**: info, estatísticas descritivas e valores ausentes  
2. **Visualização dos padrões**: histogramas, gráficos de barras e matriz de correlação  
3. **Modelagem preditiva**:  
   - Regressão Logística  
   - Random Forest  
4. **Avaliação dos modelos**: acurácia, precisão, recall, matriz de confusão  
5. **Clusterização**:  
   - K-Means para segmentar perfis de clientes  
   - Dendrograma para análise hierárquica dos grupos  
6. **Identificação de padrões de churn** e recomendações estratégicas  

## Pré-processamento
- Codificação de variáveis categóricas com one-hot encoding  
- Normalização de variáveis numéricas (StandardScaler)  
- Divisão em conjuntos de treino e validação (75% / 25%)  
- Criação de clusters com base em métricas de frequência, gastos e contratos  

## Análise dos Dados
- Clientes com **baixa frequência no último mês** apresentam risco elevado de churn  
- Contratos de **1 mês** têm maior taxa de cancelamento que planos mais longos  
- Participação em **grupos** e **programas de indicação** está ligada a maior fidelização  
- Clusters de alto risco combinam baixa frequência, contratos curtos e baixo gasto adicional  

## Resultados
- Modelos de Machine Learning alcançaram boas métricas de previsão de churn  
- **Random Forest** apresentou desempenho superior à Regressão Logística  
- Foram identificados **perfis de clientes mais propensos a sair**  
- Estratégias de marketing personalizadas podem reduzir significativamente a rotatividade  

## Aprendizados
- **Engajamento é chave**: clientes ativos e conectados socialmente permanecem mais tempo  
- **Planos longos reduzem churn**: incentivar assinaturas trimestrais ou anuais  
- **Clusters ajudam na personalização**: diferentes perfis exigem diferentes ações de retenção  
- **Ações sugeridas**:  
  - Mensagens automáticas para clientes inativos  
  - Benefícios para contratos mais longos  
  - Reforço em aulas em grupo e programas de indicação  
  - Campanhas específicas para clusters de risco
