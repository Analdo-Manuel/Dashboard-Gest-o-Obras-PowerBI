# Modelo analítico e indicadores

## Estrutura do modelo

O relatório segue uma organização dimensional: uma tabela de factos concentra os registos de produção/executação e dimensões fornecem o contexto de data, obra e produto. Esta estrutura permite reutilizar os mesmos indicadores em diferentes cortes de análise.

```text
Dim_Datas ───┐
Dim_Obras ───┼──> Fact_Producao <── Dim_Produtos
             │
        filtros e medidas
```

| Tabela | Responsabilidade no modelo |
| --- | --- |
| `Fact_Producao` | Factos de produção e medidas de execução física, financeira e de prazo. |
| `Dim_Datas` | Calendário usado para análise temporal e evolução acumulada. |
| `Dim_Obras` | Identificação e atributos das obras. |
| `Dim_Produtos` | Produtos e informação de área de negócio. |

Os nomes acima reflectem as tabelas usadas pelo relatório. Relações, tipos de dados e fórmulas DAX devem ser consultados directamente no Power BI Desktop antes de qualquer alteração ao modelo.

## Glossário de KPIs

| Indicador | Leitura recomendada |
| --- | --- |
| **% Avanço Físico** | Progresso físico das actividades no contexto filtrado. Compare-o com a referência prevista para avaliar a execução. |
| **Avanço previsto / realizado** | Comparação entre a meta do plano e a execução observada. O sentido do desvio deve ser analisado com a convenção usada no visual. |
| **Valor previsto / valor final** | Montantes planeados e observados/finais para controlo financeiro. |
| **Desvio orçamental** | Diferença entre os valores financeiros de comparação definidos no relatório. Analise o sinal e a base de comparação antes de classificar como favorável ou desfavorável. |
| **CPI** | Indicador de desempenho de custos apresentado no relatório. Interprete-o juntamente com os valores e o método de cálculo configurado no modelo. |
| **Actividades atrasadas** | Número de actividades sinalizadas como fora do prazo. |
| **% de actividades atrasadas** | Peso das actividades em atraso no total do contexto seleccionado. |
| **Atraso médio / máximo (dias)** | Intensidade típica e pior caso de atraso; úteis em conjunto, não como substitutos da lista de actividades. |
| **Curva S** | Evolução acumulada prevista e executada ao longo do tempo, utilizada para observar tendências e desvios sustentados. |

## Convenções para evolução segura

1. Mantenha chaves estáveis nas dimensões para não quebrar relações com `Fact_Producao`.
2. Use `Dim_Datas` como referência de calendário para medidas temporais.
3. Crie medidas novas em vez de alterar medidas existentes sem validar as páginas afectadas.
4. Teste os KPIs em pelo menos uma obra, um produto e o total antes de publicar.
5. Documente a regra de negócio sempre que introduzir uma nova medida ou coluna calculada.
