# Sistemas Inteligentes

Este repositório reúne os notebooks da disciplina **Sistemas Inteligentes**, com foco em estudo aplicado, experimentação e análise de resultados.

## Contexto Geral

A proposta deste material é documentar, de forma prática, com implementações de filtros, modelos e técnicas vistas na teoria, mostrando:

- modelagem matemática de problemas;
- simulação computacional;
- avaliação de desempenho com métricas;
- interpretação dos resultados.

## Conteúdo

### 1. `notebook_6_modelos_senoides_final.ipynb`

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




## Observação

É importante não tomar esse repositório como fonte principal de conhecimento e como uma fonte 100% confiável na colocação dos respectivos conteúdos, já que o objetivo aqui é apenas tentar implementar o conhecimento visto em artigos, livros, etc.
