# DataSciencePython-
common data analysis  using python
# Importando as bibliotecas 
import pandas as pd 
import numpy as np
import matplotlib.pyplot as plt
# Descrevendo os dados 
df = pd.read_csv (r'D:\Users.csv')
print (df)
df.head()
df.describe()
df.info()
df.shape
df.keys()
# Contando o total de valores únicos 
df['Invoice ID'].unique()
# Contando o total de linhas 
df['Invoice ID'].value_counts()
# Gerando gráfico de barras a partir de dados agrupados 
df.groupby(['Branch', 'Gender'])['Invoice ID'].count()
df.pivot_table(index='Branch',columns=['Gender'],aggfunc=['size']).plot(kind='bar', figsize=(15,8))
plt.show()
