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


<img width="742" height="441" alt="boxplot-qtd_transacoes-uso_percentual_credito" src="https://github.com/user-attachments/assets/8ef054f5-dc91-482e-ad9a-d646983a8cde" />


<img width="1490" height="671" alt="boxplot-uso_percentual_credito-limite_credito-valor_transacoes" src="https://github.com/user-attachments/assets/35aa12a4-1139-4407-8545-dfc012b8ca59" />


<img width="525" height="382" alt="relplot-limite_credito-valor_transacoes" src="https://github.com/user-attachments/assets/c4219385-90f5-4c76-9f35-d9a84269c1ff" />


<img width="526" height="383" alt="relplot-qtde_transacoes-valor_transacoes" src="https://github.com/user-attachments/assets/7bbc538b-6a0b-4652-859e-c2f98c43ffbf" />


<img width="891" height="295" alt="correlacao-duas_var" src="https://github.com/user-attachments/assets/04c5ece5-d357-45d6-a739-1a4023cca2d7" />


<img width="735" height="298" alt="correlacao-uma_var" src="https://github.com/user-attachments/assets/53d1e3c3-41af-4ba0-8ca2-b9ef7685861e" />


<img width="742" height="293" alt="correlacao-uma_varr" src="https://github.com/user-attachments/assets/0dd23604-90bb-48ce-a1e3-1c0cf90de07a" />

