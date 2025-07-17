# A dissertacao

Descrição do Fluxo de Análise dos Notebooks
Analise llm cruzados.ipynb e Avaliação do questionario-professores.ipynb

1. Introdução ao Processo Analítico
A condução das análises realizou-se em dois grandes eixos:

(i) a análise cruzada entre modelos de linguagem de larga escala (LLMs), onde cada LLM avalia as questões geradas pelos demais;

(ii) a análise das avaliações realizadas por professores humanos a partir de um questionário estruturado.

Ambas as frentes compartilham o objetivo de investigar a qualidade das questões geradas por IA, buscando identificar padrões, convergências, contraste nos critérios avaliados e robustez das avaliações em ambientes automatizados e humanos.

2. Resumo do Fluxograma Analítico
Segue um fluxograma simplificado das etapas principais:

Leitura e Padronização dos Dados  

→ Filtragem (remover avaliações envolvendo “Professor” nos cruzamentos automáticos)

→ Análise Exploratória Descritiva  

→ Análises Estatísticas e Testes de Hipótese  

→ Visualização Gráfica  

→ Exportação/Síntese para o Relatório

Abaixo, detalha-se cada etapa:

3. Etapas Detalhadas por Notebook
A) Notebook: Analise llm cruzados.ipynb
a. Leitura e Tratamento:

Os dados foram importados da aba "Avaliacoes_Automaticas" do Excel, contendo informações de ID, LLM gerador, LLM avaliador, tipo de prompt, critério, pontuação e análise textual automatizada.

Os nomes dos LLMs e critérios foram padronizados (capitalização, remoção de espaços e acentos).

b. Filtragem:

Foram considerados exclusivamente os cruzamentos entre LLMs (excluindo todas as linhas nas quais o Professor era o gerador ou avaliador), para garantir análise puramente automatizada e sem viés humano.

c. Análise Exploratória e Estatística:

Geradas estatísticas descritivas (médias, desvios, contagem) para cada critério, por LLM gerador e avaliador.

Realizada análise gráfica das médias de pontuação por critério.

Executados testes ANOVA para verificar diferenças estatísticas significativas entre LLMs para cada critério e pares avaliador-gerador.

Aplicados testes post-hoc (Tukey) quando necessário, detalhando as comparações par a par.

Elaborados heatmaps de médias cruzadas para visualização rápida de padrões (quem avalia quem e como).

Realizadas análises complementares:

Comparação por tipo de prompt (simples vs. meta)

Análise de rigorosidade/uniformidade dos avaliadores

Ranking dos LLMs por critério

Mapas de reciprocidade (autoavaliação × avaliação do outro)

Análise de dispersão, detecção de outliers e clusterização de padrões de avaliação.

d. Exportação e Síntese:

Resultados tabulados para facilitar a incorporação no relatório e discussão acadêmica.

B) Notebook: Avaliação do questionario-professores.ipynb
a. Leitura e Limpeza:

Carregamento das respostas de professores via arquivo Excel, focando avaliações humanas dos mesmos critérios das análises automáticas.

b. Estruturação dos Dados:

Padronização dos nomes das colunas, critérios e cruzamento entre perfil docente, LLM/Prompt, critério avaliado, e pontuação.

c. Análise descritiva e cruzada:

Cálculo das médias de avaliação para cada critério por LLM/Prompt, separadas por subgrupos docentes (nível de formação, tempo de experiência, uso prévio de IA, nível de estresse, frequência de elaboração de questões, etc.).

Geração de gráficos (barras, caixas, linhas) para cada critério segundo o perfil e o grupo de LLM/Prompt avaliado.

Aplicação de ANOVA/Kruskal-Wallis para investigar diferenças entre grupos docentes/perfil e suas avaliações.

Testes de médias e post-hoc para as principais comparações.

d. Explorações Avançadas:

Estudo de correlações entre critérios e filtros de segmentos específicos (ex: apenas pós-graduados, apenas docentes de escola pública/federal).

Análise da dispersão das notas, outliers e identificação de perfis docentes mais benevolentes ou rigorosos.

Caso aplicável, análise temporal dos envios e do índice de concordância entre avaliadores.

4. Síntese Final
Os dois noteboooks oferecem uma triangulação robusta:

De um lado, mostram o comportamento dos LLMs em avaliações recíprocas, permitindo diferenciar padrão de tolerância, rigor e possíveis vieses entre máquinas.

De outro, detalham como educadores reais avaliam tanto propostas humanas quanto automáticas, introduzindo uma perspectiva de validação contextual e humana na formação do acervo avaliativo.
