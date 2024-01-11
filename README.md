# Algoritmo para Previsão de Score de Crédito 

## Importação e Visualização da Base de Dados 
- O código inicia importando a biblioteca pandas para manipulação de dados e lê a base de dados do arquivo "clientes.csv".
- A tabela é exibida utilizando a função display.

## Verificação de Valores Vazios e/ ou Formato Incorreto
- Utiliza-se o método info() para verificar informações atuais da tabela, incluindo a presença de valores nulos.

## Transformação de Dados Categóricos em Numéricos
- As colunas de texto são convertidas em números utilizando o LabelEncoder da biblioteca scikit-learn, exceto a coluna "score_credito".
- Transformação necessária para Machine Learning.
- O progresso é verificado novamente com info().

## Escolha das Colunas para Treinamento do Modelo
- As colunas são selecionadas para treinar o modelo, sendo "score_credito" a coluna gabarito (y) e as demais sendo (x).
- Exclui-se as colunas que não serão necessárias para a análise. Ex: "id_cliente".
- Divide-se a base de dados em conjuntos de treino e teste com train_test_split.

## Treinamento de Modelos
- Dois modelos são treinados: um utilizando o algoritmo RandomForestClassifier e outro com KNeighborsClassifier.

## Avaliação da Acurácia do Modelo
- Calcula-se a acurácia dos modelos e comparamos para decidir qual tem a melhor performance.
- Utiliza-se a métrica accuracy_score para avaliar a precisão dos modelos treinados.
- Após comparação de resultados, confirmamos o modelo RandomForestClassifier

## Novas Previsões
- Carrega novos dados do arquivo "novos_clientes.csv" e realiza as mesmas transformações aplicadas à base de treino.
- Realiza previsões utilizando o modelo treinado com RandomForestClassifier.

## Importância das Características
- Identifica as características mais importantes para a previsão do score de crédito utilizando a feature_importances_ do modelo RandomForestClassifier.
- Exibe a importância de cada característica em percentagem.

## Observação
- Certifique-se de instalar as bibliotécas corretamente.
- Certifique-se de ajustar os nomes dos arquivos de entrada ("clientes.csv" e "novos_clientes.csv") conforme a necessidade do seu projeto.
