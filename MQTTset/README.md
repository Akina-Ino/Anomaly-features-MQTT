# Dataset MQTT - Detecção de Ataques DoS

Este repositório contém o dataset utilizado no projeto de análise e detecção de ataques DoS no protocolo **MQTT**, comprimido no formato `.gz` para facilitar o armazenamento e o compartilhamento.

---

## Arquivo Compactado

* **Nome do arquivo**: `mqttdataset_reduced.csv.gz`
* **Formato**: CSV (comprimido em Gzip)
* **Tamanho aproximado (comprimido)**: 7.2 MB
* **Tamanho aproximado (descomprimido)**: 59.4 MB
* **Número de linhas (amostra usada)**: 330927 linhas

---

## 🔓 Como descomprimir o arquivo

### Linux / macOS

```bash
gunzip mqttdataset_reduced.csv.gz
```

Ou:

```bash
gzip -d mqttdataset_reduced.csv.gz
```

Se quiser manter o arquivo original `.gz`:

```bash
gunzip -k mqttdataset_reduced.csv.gz
```

### Windows

1. Baixe e instale [7-Zip](https://www.7-zip.org/) ou outro descompactador.
2. Clique com o botão direito no arquivo → **"7-Zip" > "Extract Here"**.

### Python (opcional)

Você também pode descomprimir com Python:

```python
import gzip
import shutil

with gzip.open('mqttdataset_reduced.csv.gz', 'rb') as f_in:
    with open('mqttdataset_reduced.csv', 'wb') as f_out:
        shutil.copyfileobj(f_in, f_out)
```

---

## Utilização no Projeto

Este dataset foi utilizado para:

* Treinar e testar algoritmos de Machine Learning (SVM e KNN)
* Detectar padrões em ataques DoS, Flood e SlowITe
* Avaliar as features mais relevantes na camada MQTT e TCP

> A versão reduzida utilizada contém as 50.000 primeiras linhas do dataset completo.

---

## Estrutura dos dados

Algumas das colunas presentes no CSV:

* `tcp.flags`, `tcp.len`, `mqtt.msgtype`, `mqtt.qos`, `mqtt.len`
* `target` (rótulo de ataque ou tráfego normal)

---

## Licença

Este dataset é utilizado apenas para fins acadêmicos e de pesquisa. Para mais detalhes sobre a origem dos dados, consulte a documentação do projeto.

---
