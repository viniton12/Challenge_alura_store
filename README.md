
# 📊 Análise de Vendas por Loja

Este projeto tem como objetivo realizar uma **análise individual de desempenho para cada loja**, utilizando dados de vendas. A análise envolve métricas como faturamento, avaliação de clientes, custo médio de frete e visualizações gráficas para facilitar a tomada de decisão.

## 🔧 Tecnologias Utilizadas

- Python 🐍  
- Pandas 📊  
- Matplotlib 📈

---

## 📥 Etapas da Análise

### 1. Importação das Bibliotecas

```python
import pandas as pd
import matplotlib.pyplot as plt
```

### 2. Leitura dos Dados

```python
df = pd.read_csv('arquivo.csv')
```

---

## 📌 Análises Realizadas

### ✅ Faturamento Total

Função para calcular o faturamento total com base na coluna `Preço`.

```python
def faturamento(df):
    return df['Preço'].sum()
```

---

### ✅ Categorias Mais Vendidas

Utilização de `value_counts()` para identificar as categorias com maior volume de vendas.

```python
df['Categoria do Produto'].value_counts()
```

---

### ✅ Avaliação dos Clientes

Análise das avaliações recebidas:

```python
df['Avaliação da compra'].value_counts()
```

Cálculo da média das avaliações:

```python
media_avaliacao_loja = df['Avaliação da compra'].mean()
print(f'A média de avaliação da loja foi {media_avaliacao_loja:.2f}')
```

Distribuição percentual das avaliações:

```python
df['Avaliação da compra'].value_counts(normalize=True)
```

---

### ✅ Custo Médio de Frete

```python
custo_medio_frete = df['Frete'].mean()
print(f'O custo médio do frete é de R$ {custo_medio_frete:.2f}')
```

---

## 📊 Visualizações Criadas

### 📌 Faturamento por Categoria

```python
plt.figure(figsize=(15, 5))
plt.bar(faturamento_por_categoria['Categoria do Produto'], faturamento_por_categoria['Faturamento'], color='c')
plt.title('Faturamento por Categoria')
plt.xticks(rotation=90)
plt.show()
```

---

### 📌 Faturamento por Produto

```python
plt.figure(figsize=(15, 5))
plt.bar(faturamento_por_produto['Produto'], faturamento_por_produto['Faturamento'], color='g')
plt.title('Faturamento por Produto')
plt.xticks(rotation=90)
plt.show()
```

---

### 📌 Número de Vendas por Produto

```python
plt.figure(figsize=(15, 5))
plt.bar(produtos.index, produtos.values, color='skyblue')
plt.title('Número de vendas por produto', color='darkred', fontsize=15)
plt.ylabel('Quantidade', color='red')
plt.xlabel('Produto', color='red')
plt.xticks(rotation=90, fontsize=10)
plt.show()
```

---

### 📌 Comparação de Avaliações entre Lojas

```python
plt.figure(figsize=(8, 6))
plt.bar(df['Loja'], df['Avaliação'], color='#2C3E50', width=0.3)
plt.title('Comparação de avaliações das lojas', color='darkred', fontsize=15)
plt.ylabel('Nota')
plt.xlabel('Loja')
plt.grid(True)
plt.show()
```

---

### 📌 Custo Médio de Frete por Loja

```python
plt.figure(figsize=(8,6))
plt.bar(df['Loja'], df['Frete médio'], color='red', width=0.5)
plt.title('Custo Médio do Frete', color='darkred', fontsize=15)
plt.ylabel('Custo (R$)')
plt.xlabel('Loja')
plt.grid(True)
plt.show()
```

---

## 📌 Conclusão

Este projeto permitiu identificar:

- O **faturamento total** por loja e por categoria.
- As **categorias mais vendidas**.
- A **avaliação dos clientes** em termos absolutos e percentuais.
- O **custo médio de frete**.
- Diferenças de desempenho entre as lojas através de **visualizações interativas**.

---

## 📝 Relatório Final das Análises

Com base nas análises realizadas, foram obtidas as seguintes conclusões:

- **Faturamento**: A maioria das lojas apresentou um bom desempenho de vendas, mas houve variação significativa entre os produtos e categorias. Isso evidencia a importância de focar nos itens de maior faturamento.

- **Categorias Mais Vendidas**: Algumas categorias se destacam, sendo responsáveis por grande parte do volume de vendas. Estratégias de marketing e reposição podem ser otimizadas com base nesses dados.

- **Avaliação do Cliente**:
  - A média geral das avaliações foi satisfatória, indicando boa aceitação dos produtos e serviços.
  - No entanto, a distribuição das notas revela que algumas lojas ou produtos específicos precisam de melhorias.

- **Custo Médio de Frete**: Identificou-se uma variação no custo médio do frete entre as lojas. Lojas com frete mais caro podem perder competitividade se não oferecerem benefícios adicionais ao cliente.

- **Visualizações**: Os gráficos facilitaram a visualização das diferenças entre lojas, produtos e categorias. A utilização de gráficos de barras, pizza e linhas possibilitou uma análise mais dinâmica e intuitiva dos dados.

Essas análises fornecem informações valiosas para orientar **decisões estratégicas**, como ações de marketing, logística, ajustes de preços e foco em determinados produtos ou categorias.

---

## 💼 Autor

**Vinícius Calisto de Sirqueira**  
Graduando em Ciências Biológicas • Entusiasta de Dados & Visualizações  
---

