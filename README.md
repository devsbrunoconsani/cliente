## Importar bibliotecas
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline
%config InlineBackend.figure_format = 'svg'
anuncios = pd.read_csv('advertising.csv')
anuncios.head()
from pandas_profiling import ProfileReport
relatorio = ProfileReport(anuncios, title='Relatório dos Anúncios')
relatorio.to_file('relatorio_dos_anuncios_v1.html')
relatorio
