README — Porsche Sales Dashboard | Endereço do repositório público: https://cainaazevedopsico.github.io/Desafio-acelera-o-html-dados-de-porsche/
=================================

DOCUMENTO DE APOIO AO EXERCÍCIO DO CURSO
---------------------------------------
Este arquivo reúne as informações solicitadas para a entrega do projeto. Antes da submissão, substitua os campos de publicação pelos links reais do seu repositório público e da dashboard no GitHub Pages. O conteúdo pode ser aproveitado no README.md do repositório.

1. OBJETIVO DO PROJETO
---------------------

Desenvolver uma dashboard interativa em HTML para explorar uma base com 100 registros de veículos Porsche. A proposta é praticar tratamento e preparação de dados, formulação de perguntas de negócio, análise exploratória e comunicação visual dos resultados.

A dashboard permite filtrar os registros por dimensões de veículo, localização, status e pagamento. Os dados utilizados estão incorporados no próprio HTML, tornando o arquivo independente de servidor, planilha externa ou biblioteca carregada pela internet.

2. PERGUNTAS DE NEGÓCIO ESCOLHIDAS E JUSTIFICATIVAS
--------------------------------------------------

Pergunta 1 — Quais faixas de quilometragem concentram mais e menos registros?

Justificativa: a análise permite observar como os registros se distribuem conforme a quilometragem dos veículos e identificar as faixas com maior e menor frequência. A intenção é explorar possíveis padrões entre quilometragem e volume de registros, sem presumir uma relação causal. Como a base também contém registros pendentes, cancelados e em trânsito, a contagem não deve ser interpretada como quantidade de vendas concluídas.

Pergunta 2 — Qual é a variação de preço entre unidades do mesmo modelo e como ela se relaciona com a quilometragem?

Justificativa: comparar unidades do mesmo modelo ajuda a identificar a amplitude dos preços observados e a levantar possíveis fatores associados às diferenças. A quilometragem foi incluída como variável exploratória. Em uma base privada e mais completa, esse tipo de análise poderia apoiar estudos sobre negociação e descontos, mas os dados atuais não permitem afirmar que a quilometragem, isoladamente, explica as diferenças de preço nem calcular o resultado financeiro de uma negociação.

Pergunta 3 — Quais métodos de pagamento são mais populares no total e em cada estado?

Justificativa: conhecer a distribuição dos meios de pagamento pode orientar análises futuras sobre custos, taxas e possíveis oportunidades de marketing. A comparação por estado permite observar diferenças geográficas sem fragmentar excessivamente uma base pequena. Com apenas 100 registros, a análise por cidade poderia produzir grupos com poucos casos.

Análises complementares incluídas na evolução da dashboard:
- Como preço e quilometragem se distribuem conjuntamente entre os registros (gráfico de dispersão).
- Como os registros se distribuem por faixas de preço.
- Quantos registros existem por ano do modelo.
- Quais modelos aparecem com maior frequência.

Essas visualizações complementam as perguntas principais e ampliam a exploração da base, mas não substituem as ressalvas metodológicas descritas neste documento.

3. PROMPT UTILIZADO E EVOLUÇÃO ATÉ A VERSÃO FINAL
------------------------------------------------

Prompt inicial utilizado para gerar a primeira versão:

“Quero fazer uma dashboard com esses dados de vendas de carros Porsche, em HTML, com filtros por estado da venda, cidade, quilometragem em km, valor, método de pagamento, ano do modelo e modelo; análises para identificar as faixas de quilometragem mais e menos vendidas, a variação percentual de preço entre unidades do mesmo modelo e sua relação com a quilometragem, e o método de pagamento mais popular no total e por estado; interface clean e profissional inspirada na identidade visual do site oficial da Porsche, com filtros e análises em áreas separadas e organização orgânica.”

Principais mudanças solicitadas depois do prompt inicial:

1) Refinamento visual para uma apresentação mais premium, inspirada no site oficial da Porsche Brasil (https://www.porsche.com/brazil/pt/): fundo predominantemente escuro, preto e grafite, detalhes vermelhos, tons metálicos, tipografia moderna, hierarquia mais clara e aparência profissional.

2) Reorganização da interface: cards de indicadores menores e compactos, caixas com cores em vez de grandes áreas brancas, melhor aproveitamento da tela e adaptação a telas menores.

3) Preservação dos filtros, indicadores, cálculos e gráficos que já existiam. As solicitações seguintes especificaram que novos gráficos deveriam ser adicionados sem substituir ou modificar os gráficos anteriores.

4) Inclusão de quatro visualizações complementares: dispersão de preço por quilometragem; distribuição por faixas de preço; registros por ano do modelo; e ranking dos dez modelos mais frequentes.

5) Melhoria da interação nas tabelas de amplitude de preço por modelo e de método de pagamento por estado. Os cabeçalhos podem ser clicados para ordenar as informações: colunas numéricas começam do maior para o menor e colunas de texto começam em ordem alfabética. Um novo clique no mesmo cabeçalho inverte a ordenação.

6) Manutenção de uma dashboard autônoma, com os dados incorporados no HTML, filtros combináveis, gráficos atualizados pela seleção e layout responsivo.

A evolução foi feita de forma incremental: a primeira versão estabeleceu os filtros e as análises principais; as iterações seguintes priorizaram a identidade visual, acrescentaram visualizações e aprimoraram a exploração das tabelas. As fórmulas e os critérios descritivos originais foram preservados.

4. TRATAMENTO DA BASE ANTES DO USO DA IA
----------------------------------------

O tratamento dos dados originais foi realizado previamente com um script em Python. A IA foi utilizada a partir da versão sanitizada da base, e não como substituta dessa etapa inicial de preparação.

Arquivo de origem tratado: porsche_database_sanitized.xlsx.
Planilha utilizada: “Sanitized ” — o nome da aba contém um espaço ao final.
Quantidade de registros utilizada: 100.

Campos selecionados para a dashboard:
- DeliveryStatusSanitized — status da venda/entrega.
- CitySanitized — cidade.
- VehicleMileageSanitized — quilometragem.
- SalesPriceSanitized — preço.
- PayMethodSanitized — método de pagamento.
- ModelYearSanitized — ano do modelo.
- PorscheModelSanitized — modelo Porsche.
- StateSanitized — estado/UF.

Na preparação para a análise, os campos quantitativos utilizados pela dashboard são representados como valores numéricos — quilometragem, preço e ano do modelo — enquanto status, cidade, método de pagamento, modelo e estado são utilizados como categorias para filtros, agrupamentos e contagens. Os preços permanecem em dólares americanos (USD) e a quilometragem é expressa em quilômetros (km).

Somente os campos necessários às análises foram incorporados ao HTML. Dados pessoais de clientes e vendedores não foram incluídos na dashboard. Como os registros ficam embutidos no código, é importante revisar novamente o conteúdo do HTML e qualquer arquivo que venha a ser publicado antes de tornar o repositório público.

A dashboard não depende do arquivo Excel para funcionar: os 100 registros utilizados estão incorporados no próprio HTML. A planilha é a fonte de dados do projeto, mas não é uma dependência técnica da página publicada.

5. FERRAMENTA DE IA UTILIZADA
-----------------------------

Foi utilizado o ChatGPT com Canvas como ambiente de apoio à criação e à evolução da dashboard HTML. Não foi utilizado um agente com skill. O desenvolvimento foi conduzido de forma iterativa, com solicitações para criar a primeira versão, refinar o visual, acrescentar gráficos e implementar a ordenação das tabelas.

O artefato final é um arquivo HTML independente. A documentação do projeto é mantida separadamente neste arquivo de texto e deve ser aproveitada no README.md do repositório público.

6. ARQUIVOS DO PROJETO
----------------------

Arquivos de trabalho utilizados:
- porsche_database_sanitized.xlsx — planilha de origem já sanitizada; aba “Sanitized ”.
- porsche_sales_dashboard_premium.html — dashboard HTML final no ambiente local.
- Read_me_porsche_dashboard.txt — este documento de apoio, a ser utilizado como base para o README.md do repositório.

Estrutura recomendada para o repositório público:

porsche-sales-dashboard/
|-- index.html
|-- README.md
|-- screenshots/
    |-- dashboard-visao-geral.png
    |-- dashboard-filtro-aplicado.png

Para publicar no GitHub Pages, copie a versão final da dashboard para o repositório e utilize o nome index.html na raiz. Copie o conteúdo deste documento para um arquivo chamado README.md. A pasta screenshots deve conter capturas reais da dashboard em funcionamento; não mantenha referências a imagens que ainda não foram adicionadas.

A planilha Excel foi utilizada como fonte na etapa de desenvolvimento, mas não é necessária para executar a página, pois os dados estão incorporados no HTML. Não é obrigatório publicá-la no repositório. Caso decida incluí-la, revise seu conteúdo novamente e confirme que não contém dados pessoais ou confidenciais.

7. FILTROS, INDICADORES E ANÁLISES DA DASHBOARD
----------------------------------------------

Filtros combináveis disponíveis:
- Status da venda / entrega (DeliveryStatusSanitized).
- Cidade (CitySanitized).
- Quilometragem mínima e máxima, em km (VehicleMileageSanitized).
- Preço mínimo e máximo, em USD (SalesPriceSanitized).
- Método de pagamento (PayMethodSanitized).
- Ano do modelo (ModelYearSanitized).
- Modelo Porsche (PorscheModelSanitized).
- Estado / UF (StateSanitized).

Todos os filtros atualizam simultaneamente os indicadores, os gráficos e as tabelas. O botão “Limpar filtros” restaura a seleção completa.

Indicadores principais:
- Quantidade de registros na seleção atual.
- Preço médio em USD (média simples).
- Quilometragem média em km (média simples).
- Participação dos registros com status “Delivered”.

Visualizações e tabelas:

1) Faixas de quilometragem — distribuição dos registros nas faixas 0–5.000; 5.001–10.000; 10.001–20.000; 20.001–30.000; 30.001–50.000; e acima de 50.000 km. A visualização destaca as faixas com maior e menor frequência.

2) Métodos de pagamento — distribuição geral dos métodos no conjunto filtrado, com destaque para o método mais frequente.

3) Status da venda / entrega — composição dos status registrados na seleção, incluindo Delivered, In Transit, Pending, Cancelled e os demais status existentes na base.

4) Amplitude de preço por modelo — para cada modelo com pelo menos dois registros na seleção, calcula a variação entre o maior e o menor preço pela fórmula:

   (preço máximo ÷ preço mínimo − 1) × 100

   A tabela também mostra a quantidade de unidades e o intervalo entre a menor e a maior quilometragem observada para aquele modelo. Os cabeçalhos permitem ordenar as colunas.

5) Método de pagamento por estado — identifica o método mais frequente em cada UF. Quando há empate, todos os métodos empatados são exibidos. A tabela apresenta a quantidade de registros do método líder, o total no estado e a participação do método líder no total daquele estado. Os cabeçalhos permitem ordenar as colunas.

6) Preço × quilometragem — gráfico de dispersão em que cada ponto representa um registro, com preço no eixo vertical e quilometragem no eixo horizontal. A dica de contexto apresenta informações do veículo e do registro. A visualização é exploratória e não permite inferir causalidade.

7) Distribuição por faixa de preço — quantidade de registros nas faixas de US$ 50–75 mil, US$ 75–100 mil, US$ 100–125 mil, US$ 125–150 mil, US$ 150–200 mil e acima de US$ 200 mil.

8) Registros por ano do modelo — contagem de registros por ano de modelo disponível na seleção atual.

9) Modelos com mais registros — ranking dos dez modelos com maior quantidade de registros na seleção atual. Empates são apresentados em ordem alfabética.

Ordenação das tabelas dos pontos 4 e 5:
- Clique em um cabeçalho para ordenar pela coluna correspondente.
- Colunas numéricas começam em ordem decrescente (maior para menor).
- Colunas textuais começam em ordem alfabética (A–Z).
- Clique novamente no mesmo cabeçalho para inverter a ordem.
- A ordenação escolhida é mantida quando os filtros são aplicados.

8. CRITÉRIOS DE INTERPRETAÇÃO E LIMITAÇÕES
-----------------------------------------

- A base contém 100 registros.
- Os preços são apresentados em dólares americanos (USD), conforme os valores da planilha.
- A dashboard conta os registros da base, e não apenas transações concluídas. Registros pendentes, cancelados, em trânsito ou com outros status continuam incluídos, salvo quando filtrados.
- “Status da venda / entrega” corresponde a DeliveryStatusSanitized. O filtro “Estado (UF)” é uma dimensão geográfica separada.
- A amplitude de preço entre unidades do mesmo modelo não representa necessariamente desconto negociado.
- Ano, versão, opcionais, condição do veículo e outros fatores podem influenciar o preço. A quilometragem é exibida como variável exploratória; não é possível atribuir a ela, isoladamente, diferenças de preço.
- A base não contém dados suficientes sobre custos, taxas efetivas, margens, opcionais, estado de conservação ou detalhes de negociação para calcular lucro, rentabilidade ou efeitos causais.
- A análise por estado foi mantida porque a quantidade de registros é limitada para conclusões mais detalhadas por cidade.
- Os resultados são descritivos e não devem ser interpretados como estimativas de desempenho individual de vendedores.

9. COMO EXECUTAR A DASHBOARD LOCALMENTE
---------------------------------------

Abra porsche_sales_dashboard_premium.html em um navegador atualizado, como Chrome, Edge ou Firefox. Como os dados, estilos e scripts estão incorporados no arquivo, não é necessário instalar Python, iniciar um servidor ou estar conectado à internet para utilizar os filtros e as visualizações.

No repositório do GitHub, utilize index.html na raiz para que o GitHub Pages possa servir a dashboard como página inicial do site.

10. PUBLICAÇÃO E ENDEREÇOS
--------------------------

Nome sugerido para o repositório: porsche-sales-dashboard
O nome deve permanecer em letras minúsculas, sem acentos e com palavras separadas por hífens. Confirme a disponibilidade do nome na sua conta.

Status da publicação: pendente de publicação e validação pelo proprietário do projeto. Não inserir links fictícios ou utilizar o endereço do GitHub Pages no campo destinado ao link do repositório.

11. EVIDÊNCIAS PARA A APRESENTAÇÃO E PORTFÓLIO
----------------------------------------------

As evidências ajudam a demonstrar que a dashboard está publicada e funciona de verdade. Depois de publicar, abrir o endereço do GitHub Pages em um navegador e salvar pelo menos:

1) Uma captura da visão geral da dashboard, mostrando os indicadores e os gráficos.
2) Uma captura com filtros aplicados e os resultados atualizados. Um exemplo possível é selecionar o status “Delivered” e o estado “CA”; a imagem deve mostrar os filtros selecionados e os indicadores/gráficos resultantes.
3) Se possível, uma captura de uma das tabelas após clicar em um cabeçalho para demonstrar a ordenação.

Adicionar as capturas ao diretório screenshots do repositório. Conferir se os nomes dos arquivos e os caminhos registrados no README.md correspondem às imagens realmente adicionadas. As capturas devem ser feitas após a publicação, para comprovar o funcionamento da versão hospedada.

12. CHECKLIST ANTES DA SUBMISSÃO
-------------------------------

[x] A dashboard abre pelo link do GitHub Pages.
[x] Os filtros funcionam e atualizam simultaneamente os indicadores, gráficos e tabelas.
[x] Os gráficos existentes foram preservados e os gráficos complementares estão visíveis.
[x] A ordenação por clique funciona nas tabelas dos pontos 4 e 5.
[x] O repositório está na minha conta e está configurado como público.
[x] O nome do repositório está em minúsculas, sem acentos e é legível.
[x] O arquivo index.html existe na raiz do repositório e contém a versão final da dashboard.
[x] O README.md existe, contém esta documentação atualizada e não mantém campos de link em aberto.
[x] Todo arquivo e toda imagem citados no README.md existem no repositório e têm conteúdo.
[x] As capturas de tela da visão geral e de um exemplo de filtro aplicado foram adicionadas.
[x] Revisei o HTML e os arquivos que serão publicados para garantir que nenhum dado pessoal ou confidencial esteja exposto.
[ ] O link que será enviado ao curso é o do repositório público, e não apenas o link da dashboard no GitHub Pages.
[x] O link do GitHub Pages está registrado separadamente no README.md.

13. HISTÓRICO DA VERSÃO FINAL
-----------------------------

A versão premium preserva as perguntas de negócio, os filtros, os indicadores e os cálculos da primeira versão. O trabalho posterior concentrou-se no aprimoramento visual, na inclusão de quatro gráficos complementares e na ordenação interativa das tabelas. O HTML permanece autônomo e incorpora os 100 registros utilizados na análise.

Última atualização desta documentação: 20 de novembro de 2026.
