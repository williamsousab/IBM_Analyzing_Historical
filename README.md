# 📈 Stock Data Extraction and Visualization (Tesla & GameStop)

Este projeto consiste em extrair, processar e visualizar dados históricos de ações e receitas de duas grandes empresas: **Tesla (TSLA)** e **GameStop (GME)**. Ele utiliza APIs de mercado financeiro e técnicas de web scraping para gerar gráficos comparativos interativos com Python e Plotly.

---

## 🎯 Objetivo

- Extrair dados históricos de ações com `yfinance`
- Obter receitas trimestrais com web scraping
- Limpar e estruturar os dados em dataframes
- Criar dashboards interativos com `plotly`
- Comparar evolução de preço vs. receita para Tesla e GameStop

---

## 🧰 Ferramentas Utilizadas

- Python (Jupyter Notebook)
- `yfinance`
- `pandas`
- `beautifulsoup4`
- `requests`
- `plotly`
- `nbformat`
- `lxml`
- `html5lib`

---

## 🔍 Etapas do Projeto

### 1. Extração de Dados – Tesla

- Usando `yfinance` para extrair dados históricos da Tesla com `Ticker('TSLA')`
- Armazenamento em `tesla_data`, com período `max`
- Reset de índice com `.reset_index()`

### 2. Web Scraping – Receita Tesla

- Coleta da página HTML com `requests`  
- Parsing com `BeautifulSoup`
- Extração da tabela com datas e receitas
- Limpeza da coluna `Revenue` (remoção de `$`, `,`)
- Armazenamento em `tesla_revenue`

### 3. Extração de Dados – GameStop

- Mesma abordagem com `yfinance.Ticker('GME')`
- Armazenamento em `gme_data`

### 4. Web Scraping – Receita GameStop

- Coleta da tabela de receita de outra página HTML
- Processamento com lógica semelhante à Tesla
- Armazenamento em `gme_revenue`

### 5. Função de Gráfico

Uma função `make_graph()` é definida para gerar gráficos com dois eixos:

- Linha do tempo de preço da ação
- Receita trimestral acumulada

---

## 📊 Resultados

- Dois dashboards interativos com `plotly.subplots`:
  - Gráfico 1: Preço das ações da Tesla e GameStop ao longo do tempo
  - Gráfico 2: Receita trimestral de ambas as empresas
- Análises limitadas até **junho de 2021** (conforme requisito)
- Gráficos com filtro de zoom e linha do tempo sincronizada

---

## 👨‍💻 Autor

**William Sousa**  
📎 GitHub: [williamsousab](https://github.com/williamsousab)  
📎 LinkedIn: [linkedin.com/in/williamsousab](https://www.linkedin.com/in/williamsousab)

---

⭐ Curtiu o projeto? Deixe uma estrela no repositório!
