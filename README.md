# Sistemas Inteligentes

Este repositório reúne os notebooks da disciplina **Sistemas Inteligentes**, com foco em estudo aplicado, experimentação e análise de resultados.

## Contexto Geral

A proposta deste material é documentar, de forma prática, com implementações de filtros, modelos e técnicas vistas na teoria, mostrando:

- modelagem matemática de problemas;
- simulação computacional;
- avaliação de desempenho com métricas;
- interpretação dos resultados.

## Conteúdo

### 1. `Filtro de Kalman - Filtragem e Estimação`

Estudo sobre **filtragem de sinais senoidais ruidosos** com base em seis modelagens clássicas, separadas entre abordagens lineares e não lineares.

O notebook contém:

- implementação de **6 modelos de senoide**;
- separação entre **modelos lineares (5 e 6)** e **não lineares (1 a 4)**;
- uso de **Filtro de Kalman linear** (modelos lineares) e **EKF** (modelos não lineares);
- comparação de reconstrução de sinal e estimação de parâmetros (quando aplicável);
- análise de **sensibilidade à inicialização**.

Resumo:

- Modelos lineares (5 e 6): mais adequados quando a frequência é conhecida e o foco é reconstrução do sinal.

- Modelos não lineares (1 a 4): permitem estimar frequência (e amplitude no Modelo 2), mas em geral são mais sensíveis ao valor de um chute inicial.

### Resultado: reconstrução do sinal para os seis modelos

![Comparação dos sinais estimados nos 6 modelos](Filtro%20de%20Kalman%20-%20Filtragem%20e%20Estima%C3%A7%C3%A3o/six_models_of_sine_wave_images/six_models_of_sine_wave_images_20_0.png)


### 2. `Filtro de Kalman - Sintonia`

Estudo sobre **sintonia de filtros de Kalman** com base no método de Zhang et al. para identificação de covariâncias de ruído e estimação adaptativa.

O projeto contém:

- implementação do **Case 2** do artigo-base de Zhang et al.;
- aplicação do método em um problema de **posicionamento linearizado**;
- estimação de parâmetros a partir da sequência de inovações;

Resumo:

- O notebook `case2_do_zhang.ipynb` valida o método em um sistema linear conhecido.

- O notebook `posicionamento_linearizado_zhang.ipynb` aplica a ideia em um modelo local linearizado de posicionamento.

### Resultado: sintonia no problema de posicionamento

![Resultado da sintonia no problema de posicionamento](Filtro%20de%20Kalman%20-%20Sintonia/posicionamento_linearizado_zhang_images/cell_026_output_01_006.png)


### 3. `Autoencoder e PCA - Diagnóstico de Falhas`

Estudo sobre **diagnóstico de falhas baseado em dados**, comparando PCA e autoencoder undercomplete em dados do processo Tennessee Eastman.

O projeto contém:

- carregamento e preparação dos dados do processo;
- aplicação de **PCA** para detecção e análise de falhas;
- implementação de **autoencoder undercomplete**;
- comparação dos métodos nas falhas IDV(1), IDV(3) e IDV(5).

Resumo:

- O PCA é usado como abordagem clássica para redução de dimensionalidade e monitoramento estatístico.

- O autoencoder é usado como alternativa não linear para reconstrução e identificação de desvios nos dados.

### Resultado: Curvas ROC para as três falhas analisadas

<p align="center">
  <img src="Autoencoder%20e%20PCA%20-%20Diagn%C3%B3stico%20de%20Falhas/diagnostico_de_falhas_images/cell_018_output_01_007.png" alt="Curva ROC - IDV(1)" width="32%">
  <img src="Autoencoder%20e%20PCA%20-%20Diagn%C3%B3stico%20de%20Falhas/diagnostico_de_falhas_images/cell_018_output_02_008.png" alt="Curva ROC - IDV(3)" width="32%">
  <img src="Autoencoder%20e%20PCA%20-%20Diagn%C3%B3stico%20de%20Falhas/diagnostico_de_falhas_images/cell_018_output_03_009.png" alt="Curva ROC - IDV(5)" width="32%">
</p>




## Observação

É importante não tomar esse repositório como fonte principal de conhecimento e como uma fonte 100% confiável na colocação dos respectivos conteúdos, já que o objetivo aqui é apenas tentar implementar o conhecimento visto na literatura.
