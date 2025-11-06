📊 E-commerce Sales Analysis Project
🎯 Sobre o Projeto
Este projeto apresenta uma análise exploratória completa de dados de vendas de um e-commerce, focando em identificar tendências, padrões de compra e segmentos de clientes mais lucrativos. A análise foi desenvolvida em Python utilizando Jupyter Notebook/Google Colab.
🔍 Questões de Negócio Respondidas

Como foi a tendência de vendas ao longo dos meses?
Quais são os produtos mais frequentemente comprados?
Quantos produtos os clientes compram em cada transação?
Quais são os segmentos de clientes mais lucrativos?
Quais estratégias podem ser recomendadas para aumentar o lucro?

📁 Estrutura do Projeto
├── Projeto1.ipynb          # Notebook principal com toda a análise
├── Sales.csv               # Dataset de vendas (não incluído no repo)
└── README.md              # Documentação do projeto
🛠️ Tecnologias Utilizadas

Python 3.x
Pandas - Manipulação e análise de dados
Matplotlib - Visualização de dados
Seaborn - Visualizações estatísticas
NumPy - Operações numéricas
Kagglehub - Download do dataset

📊 Dataset
Os dados foram obtidos do Kaggle: An Online Shop Business Dataset
Colunas Principais:

TransactionNo (ID_Transaction) - Identificador único da transação
Date - Data da transação
ProductNo (ID_Product) - Identificador do produto
ProductName (Product_Name) - Nome do produto
Price - Preço unitário do produto
Quantity - Quantidade comprada
CustomerNo (ID_Customer) - Identificador do cliente
Country - País do cliente

🚀 Como Executar o Projeto
Pré-requisitos
bashpip install pandas matplotlib seaborn numpy kagglehub
Executando a Análise

Clone este repositório:

bashgit clone https://github.com/seu-usuario/ecommerce-sales-analysis.git
cd ecommerce-sales-analysis

Baixe o dataset do Kaggle e coloque o arquivo Sales.csv na raiz do projeto
Abra o notebook:

bashjupyter notebook Projeto1.ipynb
Ou faça upload para o Google Colab e execute as células sequencialmente.
📈 Principais Descobertas
1️⃣ Tendência de Vendas Mensal (2019)

Crescimento consistente de Janeiro a Outubro (+112,24%)
Queda abrupta em Novembro (-74,26%)
Necessidade de investigar fatores externos que impactaram as vendas em Novembro

2️⃣ Produtos Mais Vendidos
ProdutoQuantidade VendidaDestaqueWorld War 218.243Líder em Abril e OutubroRabbit Night Light14.883Líder em NovembroPopcorn Holder6.848-Assorted Colour Bird Ornament6.552-
3️⃣ Padrão de Compra por Transação

Média: 232 unidades por transação
Desvio Padrão: 1.194 unidades (5x a média)
Indica presença de clientes B2B comprando em grandes volumes

4️⃣ Segmentação de Clientes

United Kingdom domina a receita com grande margem
Concentração excessiva de receita em um único mercado
Oportunidade de diversificação geográfica

💡 Recomendações Estratégicas
📍 Expansão Geográfica

Investir em marketing e logística para mercados secundários
Reduzir dependência do mercado britânico
Explorar potencial de crescimento em outros países europeus

🎯 Estratégia de Produtos

Manter estoque robusto dos top 5 produtos
Criar bundles/kits com produtos complementares
Desenvolver campanhas específicas para produtos sazonais

📦 Gestão de Clientes B2B

Criar programa de fidelidade para grandes compradores
Oferecer descontos progressivos por volume
Estabelecer contratos de fornecimento recorrente

🔍 Investigação de Anomalias

Analisar fatores que causaram queda em Novembro 2019
Implementar monitoramento de vendas em tempo real
Criar alertas para quedas atípicas de performance

📊 Visualizações
O projeto inclui as seguintes visualizações:

📈 Gráfico de Linha: Tendência de receita mensal
📊 Gráfico de Barras Horizontal: Top produtos por mês
📉 Histograma: Distribuição de produtos por transação
📊 Gráfico de Barras: Segmentos de clientes mais lucrativos
