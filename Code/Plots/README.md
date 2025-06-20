# Imagens de Plotagem – Projeto MQTT DoS Detection

Este diretório contém gráficos gerados durante a análise dos dados e o treinamento dos modelos de Machine Learning aplicados à detecção de ataques no protocolo MQTT.

---

## Sobre as imagens

As plotagens ajudam a visualizar a distribuição dos dados, identificar diferenças entre tráfego normal e malicioso, e avaliar o desempenho dos algoritmos utilizados no projeto, como SVM e KNN.

---

## Conteúdo das imagens

| Nome do Arquivo                | Descrição                                                            |
| ------------------------------ | -------------------------------------------------------------------- |
| `heatmap_correlação.png`       | Mapa de calor com a correlação entre as features TCP/MQTT.           |
| `distribuicao_tcp_len.png`     | Distribuição dos valores da feature `tcp.len` por tipo de tráfego.   |
| `distribuicao_mqtt_len.png`    | Distribuição de `mqtt.len`, separando ataques e conexões legítimas.  |
| `importancia_features_knn.png` | Importância das features segundo o modelo KNN.                       |
| `importancia_features_svm.png` | Visualização das 10 principais features selecionadas com SVM linear. |
| `comparacao_modelos.png`       | Comparativo entre os resultados de KNN e SVM (ex: acurácia, recall). |
| `matriz_confusao_knn.png`      | Matriz de confusão do KNN com os resultados de teste.                |
| `matriz_confusao_svm.png`      | Matriz de confusão do SVM (kernel linear ou RBF).                    |
| `slowite_analise_tcp_len.png`  | Análise da feature `tcp.len` durante ataques do tipo SlowITe.        |

---

## Como gerar novamente

As imagens foram geradas por scripts em Python, utilizando as seguintes bibliotecas:

* `matplotlib`
* `seaborn`
* `scikit-learn`
* `pandas`

Para reproduzir as visualizações, utilize os notebooks ou scripts disponíveis na pasta `scripts` ou no arquivo principal de análise.

---

## Finalidade

As visualizações são utilizadas para:

* Compreender o comportamento das variáveis do dataset
* Identificar padrões relacionados aos diferentes tipos de ataques
* Apoiar a escolha das features mais relevantes
* Avaliar e comparar os modelos de classificação utilizados
