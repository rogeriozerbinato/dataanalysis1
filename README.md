# 📊 E-commerce Sales Analysis Project

## 🎯 Sobre o Projeto

Este projeto apresenta uma análise exploratória completa de dados de vendas de um e-commerce, focando em identificar tendências, padrões de compra e segmentos de clientes mais lucrativos. A análise foi desenvolvida em Python utilizando Jupyter Notebook/Google Colab.

### 🔍 Questões de Negócio Respondidas

1. **Como foi a tendência de vendas ao longo dos meses?**
2. **Quais são os produtos mais frequentemente comprados?**
3. **Quantos produtos os clientes compram em cada transação?**
4. **Quais são os segmentos de clientes mais lucrativos?**
5. **Quais estratégias podem ser recomendadas para aumentar o lucro?**

---

## 📁 Estrutura do Projeto

```
├── Projeto1.ipynb          # Notebook principal com toda a análise
├── Sales.csv               # Dataset de vendas (não incluído no repo)
└── README.md              # Documentação do projeto
```

---

## 🛠️ Tecnologias Utilizadas

- **Python 3.x**
- **Pandas** - Manipulação e análise de dados
- **Matplotlib** - Visualização de dados
- **Seaborn** - Visualizações estatísticas
- **NumPy** - Operações numéricas
- **Kagglehub** - Download do dataset

---

## 📊 Dataset

Os dados foram obtidos do Kaggle: [An Online Shop Business Dataset](https://www.kaggle.com/datasets/gabrielramos87/an-online-shop-business?resource=download)

### Colunas Principais:

- `TransactionNo` (ID_Transaction) - Identificador único da transação
- `Date` - Data da transação
- `ProductNo` (ID_Product) - Identificador do produto
- `ProductName` (Product_Name) - Nome do produto
- `Price` - Preço unitário do produto
- `Quantity` - Quantidade comprada
- `CustomerNo` (ID_Customer) - Identificador do cliente
- `Country` - País do cliente

---

## 🚀 Como Executar o Projeto

### Pré-requisitos

```bash
pip install pandas matplotlib seaborn numpy kagglehub
```

### Executando a Análise

1. Clone este repositório:
```bash
git clone https://github.com/seu-usuario/ecommerce-sales-analysis.git
cd ecommerce-sales-analysis
```

2. Baixe o dataset do Kaggle e coloque o arquivo `Sales.csv` na raiz do projeto

3. Abra o notebook:
```bash
jupyter notebook Projeto1.ipynb
```

Ou faça upload para o Google Colab e execute as células sequencialmente.

---

## 📈 Principais Descobertas

### 1️⃣ Tendência de Vendas Mensal (2019)

- **Crescimento consistente** de Janeiro a Outubro (+112,24%)
- **Queda abrupta** em Novembro (-74,26%)
- Necessidade de investigar fatores externos que impactaram as vendas em Novembro

### 2️⃣ Produtos Mais Vendidos

| Produto | Quantidade Vendida | Destaque |
|---------|-------------------|----------|
| World War 2 | 18.243 | Líder em Abril e Outubro |
| Rabbit Night Light | 14.883 | Líder em Novembro |
| Popcorn Holder | 6.848 | - |
| Assorted Colour Bird Ornament | 6.552 | - |

### 3️⃣ Padrão de Compra por Transação

- **Média**: 232 unidades por transação
- **Desvio Padrão**: 1.194 unidades (5x a média)
- Indica presença de **clientes B2B** comprando em grandes volumes

### 4️⃣ Segmentação de Clientes

- **United Kingdom** domina a receita com grande margem
- Concentração excessiva de receita em um único mercado
- Oportunidade de diversificação geográfica

---

## 💡 Recomendações Estratégicas

### 📍 Expansão Geográfica

- Investir em marketing e logística para mercados secundários
- Reduzir dependência do mercado britânico
- Explorar potencial de crescimento em outros países europeus

### 🎯 Estratégia de Produtos

- Manter estoque robusto dos top 5 produtos
- Criar bundles/kits com produtos complementares
- Desenvolver campanhas específicas para produtos sazonais

### 📦 Gestão de Clientes B2B

- Criar programa de fidelidade para grandes compradores
- Oferecer descontos progressivos por volume
- Estabelecer contratos de fornecimento recorrente

### 🔍 Investigação de Anomalias

- Analisar fatores que causaram queda em Novembro 2019
- Implementar monitoramento de vendas em tempo real
- Criar alertas para quedas atípicas de performance

---

## 📊 Visualizações Detalhadas

O projeto inclui 4 visualizações principais, cada uma respondendo a uma questão específica de negócio:

### 📈 1. Gráfico de Linha: Tendência de Receita Mensal

**Objetivo:** Identificar a evolução das vendas ao longo do ano de 2019.

**Construção:**
```python
plt.plot(df_question1_monthly['Month'], df_question1_monthly['Revenue'], marker='o')
```

**Elementos Visuais:**
- **Eixo X:** Meses de Janeiro a Dezembro de 2019
- **Eixo Y:** Receita total (Revenue) em cada período
- **Marcadores:** Círculos destacando cada ponto de dados

**Insights Obtidos:**
- Crescimento consistente de 112,24% entre Janeiro e Outubro
- Queda abrupta de 74,26% em Novembro (anomalia detectada)
- Padrão de sazonalidade identificado

**Por que Linha?** Gráficos de linha são ideais para visualizar tendências temporais e identificar padrões de crescimento/declínio.

---

### 📊 2. Gráfico de Barras Horizontal: Top Produtos por Mês

**Objetivo:** Descobrir quais produtos dominaram as vendas em cada mês.

**Construção:**
```python
sns.barplot(data=df_top_products, x='Quantity', y='Month', hue='Product_Name', palette='tab10')
```

**Elementos Visuais:**
- **Eixo Y:** Meses do ano (visualização mensal)
- **Eixo X:** Quantidade de unidades vendidas
- **Cores (hue):** Cada produto possui cor única para fácil identificação

**Insights Obtidos:**
- **World War 2:** Liderou em Abril e Outubro (18.243 unidades no ano)
- **Rabbit Night Light:** Destaque em Novembro (14.883 unidades)
- Variação mensal indica sazonalidade específica por produto

**Por que Barras Horizontais?** Facilita leitura dos rótulos mensais e permite comparação visual direta das quantidades.

---

### 📉 3. Histograma: Distribuição de Produtos por Transação

**Objetivo:** Analisar o comportamento de compra dos clientes (quantos produtos compram por vez).

**Construção:**
```python
df_question3.plot(kind='hist', bins=30, edgecolor='black', color='skyblue')
```

**Elementos Visuais:**
- **Eixo X:** Quantidade de produtos por transação
- **Eixo Y:** Frequência (número de transações)
- **30 bins:** Agrupamento em 30 intervalos para melhor visualização

**Insights Obtidos:**
- **Média:** 232 produtos por transação
- **Desvio Padrão:** 1.194 (5x maior que a média!)
- Distribuição assimétrica indica presença de clientes B2B comprando volumes muito maiores

**Por que Histograma?** Perfeito para identificar distribuição de dados numéricos e detectar outliers (valores extremos).

---

### 📊 4. Gráfico de Barras Vertical: Segmentos Mais Lucrativos

**Objetivo:** Identificar quais países geram mais receita para o e-commerce.

**Construção:**
```python
ax.bar(df_final['Country'], df_final['Revenue'], color='skyblue')
# Com rótulos de dados customizados
for rect in rects:
    label = f'{height/1000000:.1f}M'
    ax.text(rect.get_x() + rect.get_width() / 2., height + 500000, label)
```

**Elementos Visuais:**
- **Eixo X:** Países (Top 5 + categoria "Outros")
- **Eixo Y:** Receita total gerada
- **Rótulos de Dados:** Valores em milhões exibidos acima de cada barra

**Insights Obtidos:**
- **United Kingdom** domina com enorme vantagem sobre outros mercados
- Concentração excessiva de receita em um único país (risco de negócio)
- Oportunidade clara de diversificação geográfica

**Por que Barras Verticais?** Ideal para rankings e comparações categóricas simples, com rótulos facilitando leitura precisa dos valores.

---

### 🎯 Guia Rápido: Quando Usar Cada Gráfico

| Tipo de Gráfico | Melhor Para | Aplicação no Projeto |
|-----------------|-------------|---------------------|
| **Linha** | Tendências temporais | Evolução da receita mensal |
| **Barras Horizontais** | Comparações com muitas categorias | Produtos mais vendidos por período |
| **Histograma** | Distribuição de frequência | Padrão de compra por transação |
| **Barras Verticais** | Rankings e comparações simples | Receita por país |

---

## 🤝 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para:

1. Fazer um Fork do projeto
2. Criar uma branch para sua feature (`git checkout -b feature/NovaAnalise`)
3. Commit suas mudanças (`git commit -m 'Add: nova análise de correlação'`)
4. Push para a branch (`git push origin feature/NovaAnalise`)
5. Abrir um Pull Request

---

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

## 👤 Autor

**Seu Nome**

- GitHub: [@seu-usuario](https://github.com/seu-usuario)
- LinkedIn: [Seu Perfil](https://linkedin.com/in/seu-perfil)

---

## 📞 Contato

Para dúvidas ou sugestões, entre em contato através do LinkedIn ou abra uma issue neste repositório.

---

⭐ Se este projeto foi útil para você, considere dar uma estrela no repositório!
