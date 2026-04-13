<p align="center"> <img src="https://upload.wikimedia.org/wikipedia/commons/d/d4/Fiap-logo-novo.jpg" alt="FIAP Logo" width="700"/> </p>

---

## 🩺 FIAP - CardioIA | Fase 2 - Início da IA avançada: Automação Robótica, Sinapses Artificiais e Computação Quântica

## Cap 1 - Desafio Integrador: IA entre Robôs, Sinapses e Medicina

# 🫀 CardioIA – Diagnóstico Automatizado com Inteligência Artificial

> Projeto desenvolvido na FIAP com foco na simulação de sistemas inteligentes de apoio ao diagnóstico médico, utilizando NLP e Machine Learning aplicados à cardiologia.

---
## 🧾 Introdução

A evolução da Inteligência Artificial tem transformado profundamente a área da saúde, especialmente nos processos de diagnóstico clínico. Em centros médicos modernos, algoritmos já atuam como verdadeiros **“estetoscópios digitais”**, auxiliando profissionais na interpretação de dados e na tomada de decisão.

Neste contexto, o projeto **CardioIA – Fase 2** propõe a simulação de um sistema inteligente capaz de automatizar, de forma simplificada, parte do processo de diagnóstico médico. A partir da análise de descrições textuais de sintomas, o sistema é capaz de identificar padrões, associar condições clínicas e classificar o nível de risco de pacientes.

O desenvolvimento da solução envolve a aplicação prática de conceitos fundamentais de Inteligência Artificial, com destaque para **Processamento de Linguagem Natural (NLP)** e **Machine Learning**, permitindo transformar dados não estruturados em informações relevantes para apoio à decisão.

Além do aspecto técnico, o projeto também estimula uma visão crítica sobre temas essenciais no uso de IA na saúde, como **qualidade dos dados, vieses algorítmicos e governança de dados**, aproximando os alunos dos desafios reais enfrentados no mercado.

Dessa forma, o CardioIA não se limita a um exercício acadêmico, mas se posiciona como uma experiência prática que demonstra como soluções aparentemente simples, quando bem estruturadas, podem se aproximar de aplicações reais utilizadas em hospitais e centros de diagnóstico.

---

## 📌 Objetivo

Simular a automatização de diagnósticos clínicos por meio de Inteligência Artificial, reproduzindo, de forma simplificada, o funcionamento de sistemas utilizados em hospitais e centros de diagnóstico.

A solução contempla duas frentes principais:

* 🔎 **Extração de sintomas (NLP)**
* 🤖 **Classificação de risco (Machine Learning)**

---

### 🔹 Parte 1 - 📊 Criação dos Dados (Data Designer)

Nesta etapa, foi construída a base de dados utilizada em todo o projeto, simulando informações clínicas reais de forma estruturada.

Foram desenvolvidos:

Arquivo .txt contendo frases com relatos de sintomas de pacientes
Arquivo .csv com o mapa de conhecimento, relacionando sintomas a possíveis doenças
Dataset rotulado para classificação de risco clínico

Essa fase é fundamental, pois a qualidade e organização dos dados impactam diretamente no desempenho dos modelos de Inteligência Artificial.

---

### 🔹 Parte 2 -  🔎 Extração de Sintomas (NLP Simples)

Nesta etapa, foi implementado um processo de Processamento de Linguagem Natural (NLP) para interpretar frases escritas por pacientes.

O sistema realiza:

Leitura de textos contendo descrições de sintomas
Identificação de palavras-chave e expressões relevantes
Associação dos sintomas com doenças, com base no mapa de conhecimento

Essa abordagem simula, de forma simplificada, como sistemas inteligentes interpretam linguagem natural para apoiar diagnósticos médicos.

---

### 🔹 Parte 3 - 🤖 Machine Learning (Classificador de Risco)

Nesta fase, foi desenvolvido um modelo de Machine Learning para classificar o nível de risco clínico com base nas descrições textuais.
---

### 📎 Acesso ao Notebook

O desenvolvimento completo pode ser visualizado no notebook abaixo:

👉 [Abrir classificador_risco.ipynb](./classificador_risco.ipynb)

---

O processo inclui:

## ⚙️ Pipeline de Processamento Inteligente

* Leitura de frases simuladas de pacientes (`.txt`)
* Identificação de sintomas por palavras-chave (NLP)
* Associação dos sintomas a possíveis doenças via mapa de conhecimento (`.csv`)
* Vetorização das frases utilizando TF-IDF
* Treinamento de modelos de classificação (Logistic Regression, Naive Bayes, SVM e Random Forest)
* Avaliação dos modelos com métricas (acurácia, precisão, recall e F1-score)
* Seleção do modelo mais eficiente para predição de risco
* Geração de diagnóstico sugerido e classificação de risco (alto ou baixo)

O modelo final é capaz de classificar automaticamente novas frases como alto risco ou baixo risco, simulando sistemas de triagem utilizados na área da saúde.

## 🔄 Pipeline do CardioIA

![Pipeline CardioIA](./assets/imagens/cardioia_pipeline.png)

📌 **Exemplo:**

**Entrada:**

> "Estou com dor no peito e falta de ar há dois dias"

**Saída:**

> Diagnóstico sugerido: Infarto

---

### ⚙️ Metodologia

1. Leitura do dataset
2. Análise exploratória
3. Separação de variáveis (X e y)
4. Vetorização com TF-IDF
5. Divisão treino/teste (80/20)
6. Treinamento de modelos
7. Avaliação de desempenho
8. Seleção do melhor modelo
9. Testes com novas frases

---

### 🧪 Dataset

| frase                        | situacao    |
| ---------------------------- | ----------- |
| "dor no peito e falta de ar" | alto risco  |
| "leve incômodo nas costas"   | baixo risco |

📊 Total: **20 registros**

---

### 🔍 Vetorização (TF-IDF)

* Conversão para minúsculas
* Remoção de acentos
* Uso de **unigramas e bigramas**

---

### 🤖 Modelos Avaliados

* Logistic Regression
* Naive Bayes
* Linear SVM
* Random Forest

---

### 📊 Resultados

| Modelo              | Acurácia | F1-score |
| ------------------- | -------- | -------- |
| 🥇 Linear SVM       | **1.00** | **1.00** |
| Logistic Regression | 0.75     | 0.73     |
| Naive Bayes         | 0.75     | 0.73     |
| Random Forest       | 0.75     | 0.73     |

📌 **Modelo selecionado:** Linear SVM

---

### 🚀 Testes

**Entrada:**

> "dor intensa no peito e falta de ar"

**Saída:**

> 🔴 Alto risco

**Outros exemplos:**

* "cansaço leve e tontura" → 🟢 Baixo risco
* "palpitação e suor frio" → 🔴 Alto risco

---

### ⚠️ Limitações

* Dataset pequeno
* Possível overfitting
* TF-IDF não captura contexto profundo

---

### 🔮 Evoluções Futuras

* Uso de modelos como BERT
* Bases de dados maiores
* Redes neurais
* Validação cruzada

---

## ⚙️ Como Executar

### 🔧 Instalação

```bash id="6bg9my"
pip install pandas scikit-learn jupyter
```

---

### ▶️ Rodar NLP

```bash id="iv8hws"
jupyter notebook codigo/extracao_sintomas.ipynb
```

---

### ▶️ Rodar Machine Learning

```bash id="txq2xg"
jupyter notebook codigo/classificador_risco.ipynb
```

---

## 🎥 Vídeo de Demonstração

🔗 **Link:**
👉 *[INSERIR LINK DO YOUTUBE AQUI]*

---

## 📁 Estrutura do Projeto

```
cardioia-diagnostico-automatizado/
│
├── dados/
│   ├── frases_sintomas.txt          # 10 relatos reais de pacientes para teste
│   ├── mapa_sintomas_doencas.csv    # Mapa de conhecimento (Sintoma -> Doença)
│   └── dataset_risco.csv            # Base rotulada para treino do modelo de ML
│
├── notebooks/
│   ├── extracao_sintomas.ipynb      # Parte 1: Script de extração e lógica de busca
│   └── classificador_risco.ipynb    # Parte 2: Treinamento e avaliação do modelo ML
│
├── docs/                            # Documentação adicional e imagens
├── requirements.txt                 # Dependências do projeto
└── README.md
│
└── images/
      └── matriz_confusao.png
      └── cardioia_pipeline.png
---

### 🔬 Conclusão

Este projeto demonstrou a aplicação de técnicas de Processamento de Linguagem Natural (NLP) e Machine Learning na classificação de risco clínico a partir de descrições textuais de sintomas.

A utilização de vetorização TF-IDF (com unigramas e bigramas) permitiu a transformação eficiente dos dados textuais em representações numéricas, viabilizando o treinamento de modelos supervisionados. Entre os algoritmos avaliados, o modelo **Linear SVM** apresentou o melhor desempenho, destacando-se pelo equilíbrio entre precisão e recall.

Os resultados, incluindo a análise da matriz de confusão, evidenciaram a capacidade do modelo em distinguir adequadamente entre diferentes níveis de risco, com baixa taxa de erro no conjunto avaliado.

Entretanto, limitações como o tamanho reduzido da base de dados e a ausência de modelagem semântica mais profunda indicam oportunidades de melhoria. Como trabalhos futuros, recomenda-se a utilização de bases mais robustas e a adoção de técnicas mais avançadas, como modelos baseados em embeddings e redes neurais.

De forma geral, o estudo valida a viabilidade do uso de abordagens baseadas em NLP e Machine Learning para apoio à classificação de risco em cenários simulados da área da saúde.
---

## 👥 Integrantes

| Nome            | RM       | Parte no Projeto                              |
|-----------------|----------|-----------------------------------------------|
| João            | RM565999 | Extração de Sintomas (NLP Simples)            |
| Endrew Alves    | RM563646 | Criação dos Dados (Data Designer)             |
| Tayná Esteves   | RM562491 | Machine Learning (Classificador)              |
| Carlos Eduardo  | RM566487 | Documentação e Organização (GitHub)           |

---

# 👥 Organização da Equipe

O desenvolvimento do projeto **CardioIA** foi estruturado em etapas, com responsabilidades bem definidas entre os integrantes, seguindo uma abordagem colaborativa.

---

## 🧩 Divisão de Papéis

### 👤 Endrew Alves — Criação dos Dados (Data Designer)

Responsável pela construção e organização da base de dados do projeto.

- Criação das frases simulando relatos de pacientes  
- Estruturação do mapa de conhecimento (sintomas → doenças)  
- Montagem do dataset para classificação de risco  

---

### 👤 João — Extração de Sintomas (NLP Simples)

Responsável pela implementação da lógica de interpretação textual.

- Leitura das frases de entrada  
- Identificação de sintomas por palavras-chave  
- Associação com possíveis diagnósticos  

---

### 👤 Tayná Esteves — Machine Learning (Classificador)

Responsável pelo desenvolvimento do modelo de classificação de risco.

- Vetorização com TF-IDF  
- Treinamento dos modelos de Machine Learning  
- Avaliação de desempenho  
- Seleção do melhor modelo  

---

### 👤 Carlos Eduardo — Documentação e GitHub

Responsável pela organização final do projeto e entrega.

- Estruturação do repositório no GitHub  
- Criação e padronização do README.md  
- Documentação técnica e explicativa  
- Produção do vídeo demonstrativo  

---

## 🤝 Metodologia de Trabalho

A equipe seguiu uma abordagem baseada em divisão modular, onde cada integrante foi responsável por uma etapa específica do pipeline de Inteligência Artificial, garantindo:

- Organização do desenvolvimento  
- Clareza nas responsabilidades  
- Integração eficiente entre as etapas  

Essa estrutura permitiu a construção de uma solução coesa, simulando o funcionamento de projetos reais na área de tecnologia e saúde.

---


## 🚀 Diferenciais

* Simulação de diagnóstico com IA
* Uso de NLP aplicado à saúde
* Classificação de risco automatizada
* Estrutura pronta para evolução

---

## 📚 Considerações Finais

O projeto demonstra como técnicas acessíveis de Inteligência Artificial podem ser aplicadas na área da saúde, auxiliando na triagem e apoio à decisão clínica.

Mais do que um exercício acadêmico, o CardioIA representa uma base sólida para aplicações reais em sistemas inteligentes de diagnóstico.

---

📌 *Projeto desenvolvido para a Fase 2 do PBL – CardioIA (FIAP).*


---

# 🏫 Instituição

**FIAP — Faculdade de Informática e Administração Paulista**

Projeto acadêmico desenvolvido no contexto da disciplina de Inteligência Artificial aplicada a dados.

Ano: **2026**
