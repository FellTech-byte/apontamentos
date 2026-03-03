Dashboard de Gestão de Qualidade e Segurança (Integração SnagR)
Este projeto consiste numa aplicação frontend de alto desempenho desenvolvida para a visualização avançada de métricas operacionais, indicadores de desempenho (KPIs) e gestão de apontamentos (Snags) de múltiplos projetos de construção. A ferramenta consome dados diretamente de ficheiros .jsonl para criar relatórios visuais e gerir evidências fotográficas.

🚀 Principais Funcionalidades
Métricas e KPIs Dinâmicos: Acompanhamento em tempo real do volume de apontamentos abertos, fechados, assinados e a taxa global de resolução de cada projeto.

Filtros de Análise Temporal e Espacial: Capacidade de filtrar ocorrências por "Data Spotted", ano, mês e projeto específico (ex: Hotel, Centro Médico, Ensino, Residencial, Embasamento).

Visualização Avançada de Dados (Gráficos):

Histograma de volume mensal de apontamentos.

Gráfico de linha traçando a evolução temporal da taxa de resolução.

Matriz de dispersão correlacionando o volume de itens com o tempo médio de resolução (SLA).

Ranking em barras dos locais mais críticos da obra.

Módulo de Galeria e Fichas Técnicas Integradas:

Foco Analítico: Carrossel fotográfico para análise individual de defeitos através do ID.

Grade de Imagens: Mosaico com infinite scroll para navegação fluida em grandes volumes de imagens alojadas nos servidores do projeto.

Fichas Técnicas Detalhadas: Painel lateral com lista de itens que, ao serem selecionados, revelam o relatório completo do apontamento (SLA, grupo responsável, localização exata e descrição).

Importação Offline: Permite que os gestores importem os seus próprios relatórios .jsonl diretamente através da interface, garantindo o funcionamento offline do dashboard.

🛠️ Stack Tecnológico
A aplicação foi concebida para ser leve, sem a necessidade de um backend complexo, operando inteiramente no navegador do utilizador:

Estrutura: HTML5 e JavaScript (Vanilla ES6+).

Estilização UI: Tailwind CSS (importado via CDN) para uma interface responsiva e componentes estilo Glassmorphism.

Motor de Gráficos: Chart.js juntamente com plugins (chartjs-chart-matrix, chartjs-plugin-datalabels).

Tipografia: Família Inter providenciada pelo Google Fonts.

📂 Estrutura de Ficheiros e Integração de Dados
A base do sistema assenta na leitura de ficheiros estruturados linha a linha. Para que o dashboard funcione plenamente, é esperado que exista a seguinte correlação de ficheiros na pasta raiz:

index.html (Ficheiro principal da aplicação)

Centro medico.jsonl

Hotel.jsonl

Ensino.jsonl

Residencial.jsonl

Embasamento.jsonl

Snags_Unificado_CM.jsonl

Nota sobre a Estrutura JSONL: Cada linha dos ficheiros .jsonl deve conter um objeto JSON válido representando um Snag, com chaves como SnagID, Spotted, Status, Category, Defect, e Location para a correta extração e formatação visual dos relatórios.