# Teste-Python
Olá, irei apresentar as resoluções para os desafios apresentados no teste. 

A resolução foi pensada de forma a otimizar tempo de execução e melhor desempenho.


A primeira coisa a ser realizada é baixar as aplicações de python e do anaconda se você não as possuir instaladas anteriormente. 


Após a instalação, foi criado um ambiente virtual (virtual environment) no prompt de comando do Anaconda com o nome connep.


#Foram utilizados os seguintes comandos para criação do venv:

conda create --name connep python=3.6

#Para ativar o venv foi digitado o seguinte comando:

conda activate connep

#Para verificar o que está instalado no venv foi digitado o seguinte comando:

conda list

#Foi instalada as seguintes bibliotecas e aplicações com os respectivos comandos:

pip install pandas

pip install xlrd

pip install openpyxl

pip install jupyter notebook

#Após a instalação do jupyter notebook, digitei o comando:

jupyter notebook

-A tela de aplicação Web do Jupyter Notebook é inicializada e comecei a resolver os problemas propostos.

-Criei uma pasta com o nome connep e dentro da mesma coloquei o arquivo csv  “data.csv”, disponibilizado.

-Abrir a pasta connep no jupyter notebook e dentro dela criei um arquivo de ipynb, clicando em: >> "new" >> python 3, conforme imagem, para iniciar as aplicações.

-![image](https://github.com/Maximiliano-Costa/Teste-Python/assets/131134899/0e2f68fd-a6f5-4646-be84-27640968e325)

#O primeiro desafio proposto foi: Imprimir as informações contidas no arquivo na tela de forma organizada como tabela.

-Para resolução do mesmo utilizei os seguintes códigos:

1 - import pandas as pd

2 - df = pd.read_csv("data.csv", sep=",")

3 - display(df)

#O segundo desafio proposto foi: Salvar em um arquivo JSON as informações das 3 primeiras linhas de dados do arquivo importado.

-Para resolução do mesmo utilizei os seguintes códigos:

#Visualizar as linhas filtradas:

1 - df_linhas = df.iloc[:3]

2 - display(df_linhas)

#Salvar arquivo no formato JSON:

3 - datajson = df_linhas.to_json('datajson.json')

#O terceiro desafio proposto foi: Eliminar a linhas que contenham dados nulos ou em branco em qualquer posição da tabela e salvar o resultado em um arquivo excel.

-Para resolução do mesmo utilizei os seguintes códigos:

#Visualizar a tabela:

1 - import pandas as pd

2 - df = pd.read_csv("data.csv", sep=",")

3 - display(df)

#Apagar as linhas null e visualizar o resultado:

4 - df = df.dropna()

5 - display(df)

#Salvar arquivo novo no formato xlsx:

6 - data_excel = df.to_excel("data_excel.xlsx")

#O quarto desafio proposto foi: A partir desse novo arquivo, formar um outro arquivo excel com apenas os dados das colunas Suburb, Address, Rooms, Price, Postcode, Car, YearBuilt, Regionname. Onde a primeira coluna desse novo arquivo deve se a Postcode.

-Para resolução do mesmo utilizei os seguintes códigos:

#Importar biblioteca, realizar a filtragem:

1 - import pandas as pd

2 - df_excel = pd.read_excel("data_excel.xlsx", engine='openpyxl')

3 - df_new_excel = df_excel.iloc[:,[10,1,2,3,5,13,16,20]]

#Mostrar resultado da nova tabela:

4- display(df_new_excel)

#Salvar novo arquivo xlsx com a filtragem realizada:

5 - df_new_excel = df_new_excel.to_excel("data_new_excel.xlsx")

#O quinto desafio proposto foi: Criar uma outra aplicação em python que possibilite deletar ou renomear um arquivo

-Para resolução do mesmo, criei um arquivo csv na pasta connep com o nome “datac.csv” e utilizei os seguintes códigos:

#Importar a biblioteca e visualizar os arquivos existentes na pasta:

1 - import os

2 - arquivos = os.listdir()

3 - print(arquivos)

#Renomeando o arquivo:

4 - os.rename('datac.csv', 'teste_renomeado.csv')

#Deletando o arquivo:

5 - os.remove('teste_renomeado.csv')

Agradeço sua atenção.
