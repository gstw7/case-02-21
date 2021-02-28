Organização do projeto
------------

    ├── LICENSE
    ├── Makefile           
    ├── README.md          
    ├── data
    │   ├── interim        
    │   ├── raw            
    │  
    ├── pdf
    ├── models            
    │
    ├── notebooks
    │    └── dependencies                                
    │  
    ├── figures  
    │
    ├── requirements.txt 
    │                         
    └──
--------
## Requisitos
- Python 3.8
- Jupyter Notebook

## Como rodar?

1. Clonar o repositório para sua máquina;
2. Dentro da pasta do repositório execute no terminal ou prompt de comando: ```pip install -r requirements.txt```; 
Obs.: Recomendo estar utilizando um ambiente virtual para a execução do comando acima.
3. Dentro da pasta do repositório execute no terminal ou prompt de comando: ```jupyter notebook```;
4. Navegar até a pasta **notebooks** e executar os arquivos com extensão .ipynb na respectiva ordem da numeração.
---
### Rodando somente o modelo em uma nova base

Caso queira utilizar o modelo com novos dados.
Dentro da pasta **models** encontra-se os dois modelos propostos:
1. Modelo do primeiro exercício: modelo_classificacao.sav
2. Modelo do segundo exercício: modelo_nlp.sav

Ofereça para o modelo 1. novos dados com as seguintes colunas:
- Pred_class; **int** 
- probabilidade. **float**

Obs.: Sem valores nulos.

Exemplo de como executar dentro do jupyter notebook:
```py
import pickle
modelo = pickle.load(open('../models/modelo_classificador.sav', 'rb'))
modelo.predict(X[0:1])
```
---
Ofereça para o modelo 2. novos dados com as seguintes colunas:
- letra; **object**
- artista. **object**

Obs.: Sem valores nulos.

Exemplo de como executar dentro do jupyter notebook:
```py
import pickle
modelo = pickle.load(open('../models/modelo_nlp.sav', 'rb'))
modelo.predict(X[0:1])
```