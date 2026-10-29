# Visão geral do relatório

## Finalidade

O dashboard consolida o acompanhamento de obras de construção civil numa experiência de análise única. O seu foco é permitir que equipas de gestão comparem plano e execução, detectem desvios cedo e aprofundem a análise por obra, produto e área de negócio.

O ficheiro do relatório é [../powerbi/project_v1.pbix](../powerbi/project_v1.pbix) e contém cinco páginas de análise.

## Páginas do relatório

| Página | Finalidade | Exemplos de leitura |
| --- | --- | --- |
| **Avanço Físico** | Acompanhar a execução das actividades. | Compare o avanço previsto com o realizado e identifique obras ou actividades que exigem intervenção. |
| **Avanço Financeiro** | Controlar valores e desempenho de custos. | Analise os montantes previstos e finais, os desvios e o CPI no contexto seleccionado. |
| **Prazos e Atrasos** | Medir o cumprimento do cronograma. | Observe a quantidade e a percentagem de actividades atrasadas, bem como os atrasos médio e máximo. |
| **Áreas de Negócio** | Comparar o desempenho entre segmentos. | Filtre por área/produto para localizar diferenças de execução física e financeira. |
| **Análise de Curva S** | Comparar evolução acumulada no tempo. | Procure afastamentos persistentes entre a trajectória planeada e a executada. |

## Fluxo de análise sugerido

1. Comece em **Avanço Físico** para validar o estado geral da execução.
2. Passe para **Prazos e Atrasos** quando houver atraso ou menor progresso do que o esperado.
3. Verifique o impacto em **Avanço Financeiro**.
4. Utilize **Áreas de Negócio** para encontrar o segmento que explica o desvio.
5. Confirme a tendência na **Curva S**, sempre no mesmo contexto de filtros.

## Cuidados na interpretação

- Leia os cartões e gráficos no contexto dos filtros activos; uma selecção numa visualização pode alterar as restantes.
- Um valor agregado favorável pode ocultar desvios relevantes numa obra ou actividade específica. Faça a desagregação antes de concluir.
- A Curva S mostra tendência acumulada; combine-a com a página de prazos para investigar a causa operacional de um desvio.
- A qualidade da análise depende da actualidade e consistência das fontes carregadas no modelo.
