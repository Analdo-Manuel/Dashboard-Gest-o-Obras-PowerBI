# Guia de utilização e actualização

## Abrir o relatório

1. Instale o Power BI Desktop.
2. Abra [../powerbi/project_v1.pbix](../powerbi/project_v1.pbix).
3. Aguarde o carregamento do modelo e seleccione uma página na navegação inferior.

## Explorar os dados

- Use os segmentadores disponíveis para delimitar o período, a obra, o produto ou a área de negócio.
- Clique numa categoria, barra ou ponto de gráfico para aplicar selecção cruzada às outras visualizações.
- Passe o cursor sobre uma visualização para consultar detalhes no *tooltip*.
- Para regressar ao total, limpe as selecções e filtros aplicados.

## Actualizar dados

1. No Power BI Desktop, seleccione **Página Inicial > Actualizar**.
2. Se solicitado, valide ou actualize as credenciais em **Ficheiro > Opções e definições > Definições da origem de dados**.
3. Confirme se os valores e o período mais recente são coerentes antes de guardar.

As origens de dados e respectivas credenciais não estão documentadas no repositório. Não publique ficheiros com palavras-passe, tokens ou dados sensíveis. Se alterar uma origem, registe a decisão e verifique se a estrutura esperada pelo modelo foi preservada.

## Publicar uma versão actualizada

Antes de publicar no Power BI Service ou distribuir o `.pbix`, confirme:

- o período de actualização e a completude dos dados;
- os filtros, títulos e números dos cartões;
- os relacionamentos e medidas afectados por qualquer alteração de esquema;
- as permissões de acesso e a classificação dos dados;
- que as imagens e navegação continuam funcionais.

## Resolução rápida de problemas

| Situação | Verificação inicial |
| --- | --- |
| A actualização falha | Confirme rede, credenciais, permissões e disponibilidade da origem. |
| Um visual está vazio | Remova filtros e confirme se existe informação para o período/contexto seleccionado. |
| Valores inesperados | Compare o contexto de filtro, a granularidade e a data de actualização. |
| Alterações quebram a página | Reveja os nomes de colunas, tipos de dados, relações e medidas que dependem deles. |
