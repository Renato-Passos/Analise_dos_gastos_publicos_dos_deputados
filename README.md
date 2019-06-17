# Analise_dos_gastos_publicos_dos_deputados
Projeto proposto pelo professor Masanori, trata-se de uma análise e organização de dados.

## Fonte dos dados
Extraímos os dados do site oficial da Câmara Legislativa Federal.

## Bibliotecas
Utilizamos as seguintes:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sb
```

## Definindo arquivo a ser trabalhado

```python
gastos = pd.read_csv('tabelaComparativa.csv')
```

### Como foram definidas as informações na tabela

```python
gastos= pd.read_csv(r'C:\Users\Renato\tabelaComparativa.csv', error_bad_lines=False, low_memory=False, delimiter=';', encoding='latin-1', decimal=',')
```

## Relacionamos os valores gastos com os nomes

#### Gastos

```python
['Gastos'].value_counts()
```

#### Nomes

```python
gastos.groupby("Nome").mean()["Gastos"].sort_values().nlargest(25)
```

## Elaboração dos gráficos

#### Usamos as informações tratadas para criação de 4 gráficos:

1. Despesas individuais;
2. Despesas por partido;
3. Distribuição por Unidade Federativa;
4. Descrição dos Estados que mais gastaram;
