
# TrackZone - IA para Organização Inteligente de Motos em Pátios

## 🎯 Problema

Em pátios de filiais, motos são distribuídas de forma manual, o que gera desorganização, aumento do tempo de localização e erros no posicionamento de veículos. O objetivo do projeto é automatizar essa distribuição usando inteligência artificial.

## 💡 Solução

Utilizamos machine learning para prever a **zona ideal** do pátio para cada moto com base no seu **status atual**. Essa previsão otimiza o espaço físico, melhora a rastreabilidade e reduz falhas humanas.

---

## 🧠 Técnicas e Arquitetura de IA

### 🧩 Modelos Testados
- KNN
- Regressão Linear
- MLP (Rede Neural Multicamadas)

### ✅ Modelo Escolhido: **MLP com Keras**
```python
model = Sequential([
    Input(shape=(1,)),
    Dense(64, activation='relu'),
    Dense(64, activation='relu'),
    Dense(32, activation='relu'),
    Dense(n_classes, activation='softmax')
])
```

Usamos ReLU nas camadas ocultas e Softmax na camada de saída. A rede foi treinada com `categorical_crossentropy` e otimizada com `Adam`.

---

## 🛠️ Frameworks e Bibliotecas

| Biblioteca         | Finalidade                                      |
|--------------------|-------------------------------------------------|
| `pandas`           | Manipulação de dados                            |
| `numpy`            | Operações matemáticas                           |
| `scikit-learn`     | Pré-processamento e validação                   |
| `tensorflow/keras` | Criação e treinamento de redes neurais          |
| `matplotlib`       | Visualização de métricas (opcional)             |

---

## 📊 Base de Dados

A base simula motos cadastradas no sistema, contendo os campos:

- `status`: Reparo simples, Defeito no motor, etc.
- `zona_ideal`: BOX_RAPIDO, RAMPA_MANUTENCAO, PÁTIO, etc.

Foram aplicados `LabelEncoder` e `to_categorical` para o processamento.

---

## 📈 Resultados

- Acurácia final do modelo: ~85%
- Relatório de classificação gerado com `classification_report`
- Estratégia de validação: `train_test_split` com 20% de teste

---

## 🎥 Link do Pitch

➡️ [Inserir link do vídeo no YouTube aqui]

---

## 👥 Desenvolvedores

- Leticia Cristina Dos Santos Passos RM: 555241
- André Rogério Vieira Pavanela Altobelli Antunes RM: 554764
- Enrico Figueiredo Del Guerra RM: 558604

