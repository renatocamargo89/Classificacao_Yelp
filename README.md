# Classificacao_Yelp
O objetivo desse modelo é determinar se a avaliação de um usuário do Yelp ao Taco Bell terá impacto ou não na comunidade a partir da
base de dados Yelp (https://www.yelp.com/dataset). A métrica de impacto que criamos é o somatório de marcações de “Cool”, “Funny” e “Useful” de uma avaliação.

Nosso primeiro passo será uma análise descritiva do impacto das avaliações do Taco Bell para determinar o corte do que é uma avaliação com impacto e o que não é.

Uma vez com essa definição, vamos criar um modelo classificatório baseado nas características desses usuários para determinar se sua avaliação da nossa loja vai ter impacto ou não. Para criação do modelo vamos testar os modelos: Regressão logística (com e sem ajuste de LASSO), Random Forest e SVM. A métrica de sucesso será a AUC (área abaixo da curva ROC).

Uma vez definido o modelo, será determinado o ponto de corte ótimo. Para trabalhar tanto Especificidade quanto Sensibilidade, trabalharemos com o ponto ótimo entre os dois que maximiza a distância da linha de identidade (diagonal), seguindo a metodologia de Youden

Por fim, vamos aplicar o modelo na base de usuários que ainda não fizeram avaliação ao Taco Bell, para determinar se sua avaliação terá impacto ou não. Usaremos esse indicador como filtro para as demais etapas do trabalho.
