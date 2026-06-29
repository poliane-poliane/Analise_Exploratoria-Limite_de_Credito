# Análise Exploratória de Crédito: Comportamento e Limites

Este projeto apresenta uma análise exploratória completa de dados sobre a utilização de limites de crédito. O objetivo principal foi investigar padrões de consumo, identificar o perfil dos usuários e, fundamentalmente, responder à pergunta: *"Existe uso excessivo do limite de crédito em algum grupo específico?"*

Através de técnicas de ciência de dados em Python, exploramos a relação entre variáveis demográficas e o comportamento financeiro, chegando a conclusões que desafiam a intuição sobre o que realmente causa o uso excessivo de crédito.

##  Metodologia e Ferramentas
A análise foi conduzida seguindo um pipeline de tratamento e visualização de dados:
* **Limpeza e Tratamento:** Preparação do dataset, tratamento de valores ausentes e normalização de variáveis categóricas.
* **Visualização:**
    * **Boxplots:** Ferramenta central para comparar a distribuição de uso percentual, permitindo a detecção de *outliers* através da regra de Tukey (1.5 * IQR).
    * **Histogramas:** Utilizados para identificar a distribuição de frequência e assimetria das variáveis numéricas.
    * **Relplots:** Exploração de relações multivariadas entre o uso do limite e categorias demográficas.
    * **Matriz de Correlação (Heatmap):** Quantificação das relações lineares entre variáveis numéricas para identificar os fatores de maior impacto no consumo.

##  Insights da Análise Demográfica
Os dados segmentados por variáveis categóricas revelaram comportamentos distintos:
* **Sexo:** Identificamos um padrão de consumo discrepante. Enquanto a maioria dos homens utiliza o crédito de forma moderada (mediana de ~41%), o público feminino apresenta uma mediana mais elevada (135%), indicando que mais da metade das mulheres neste dataset opera acima do limite concedido.
* **Escolaridade:** Diferente do esperado, o nível de escolaridade tem baixo poder preditivo sobre o uso do limite, apresentando medianas de consumo muito similares entre os grupos.
* **Estado Civil:** Observou-se que pessoas solteiras tendem a consumir uma fatia maior do limite (mediana ~83%) em comparação aos casados (~69%), sugerindo diferenças nos hábitos de consumo e responsabilidades financeiras.

##  Conclusão Geral: Há mesmo Gasto Excessivo?
Ao cruzarmos os dados demográficos com as variáveis transacionais, chegamos a uma conclusão fundamental: **o uso excessivo do limite de crédito não está primariamente associado a um gasto absoluto descontrolado, mas sim a um desalinhamento entre o limite concedido e o perfil de gasto do cliente.**

Nossa análise hierarquizou os fatores que modulam o uso percentual do limite:
1. **Fator Primário (Limite de Crédito):** Identificamos uma forte correlação inversa entre o limite disponível e o uso percentual. Clientes com limites baixos tendem a utilizar frações muito maiores do crédito (frequentemente superando 100%), independentemente do volume absoluto transacionado.
2. **Fator Secundário (Valor das Transações):** O gasto absoluto possui uma associação moderada. Gastos elevados só resultam em uso percentual "excessivo" quando o limite é incompatível com o padrão de consumo.
3. **Fator Terciário (Quantidade de Transações):** A frequência das operações possui o menor impacto sobre o uso percentual do limite.

**Conclusão Final:** O "uso excessivo" está concentrado em grupos com limites mal dimensionados. Clientes com limites adequadamente ajustados conseguem sustentar volumes altos de transação sem apresentar uso percentual excessivo. Portanto, estratégias de concessão de crédito devem priorizar o ajuste inteligente de limites ao perfil de consumo, em vez de focar apenas na restrição de gastos.

##  Apêndice: Curiosidades
Para quem deseja explorar os detalhes finos desta análise, o notebook contém uma seção especial abordando:
* **Dispersão e Homogeneidade:** Por que o comportamento masculino é mais previsível enquanto o feminino apresenta maior dispersão.
* **O papel dos Outliers:** Como os valores extremos (chegando a 507% do limite) distorcem as médias e por que a mediana é a métrica mais confiável aqui.
* **Reflexões Financeiras:** Por que limites baixos podem ser contraproducentes para a saúde financeira do cliente e para a precisão da avaliação de crédito.

---
*Projeto desenvolvido como parte do módulo final de Python para Análise de Dados.*
