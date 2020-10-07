# NLP-predict-client-evaluation

Problema proposto

O problema consiste em prever a nota de avaliação dos clientes de um website de ecommerce, com base nos dados de avaliações (train_df.csv).

Para isso foi fornecido uma tabela de dados de empresa de ecommerce com mais de 100 mil avaliações de clientes. A base oferece informações sobre o perfil do revisor, como sexo, idade e localização geográfica.

Para cumprir com o objetivo:
- Utilizamos principalmente o texto e o titulo da review.
- Não identificamos fortes correlações com as outras informações.
- Retiramos pontuação e sinais diacrítico do texto.
- Utilizamos o algoritimo snowball para realizar stemming no texto. (O algoritimo rslps tambem foi testado)
- Pegamos o texto e passamos por um vetorizador utilizando a tecnica de TF-IDF com unigran e bigrans. (Testamos com outras variações também)
- O modelo que apresentou os melhores resultados foi o Linear Regression. (Embora o XGBoost tambem tenha se portado bem)
- Conseguimos em media uma acurácia de 64,97% em uma rodada de 5-fold cross validation com o nosso modelo.

Como curiosidade:
- Conseguimos uma acurácia de 93,27% utilizando um modelo com os mesmos parametros se nosso objetivo fosse somente identificar se o revisor recomendaria o produto para um amigo ou não.