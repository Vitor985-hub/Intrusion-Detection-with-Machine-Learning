# Intrusion Detection with Machine Learning

Este projeto aplica técnicas de **Machine Learning supervisionado** para detecção de intrusão em redes, utilizando o dataset público **CICIDS2017**. O foco do trabalho é a construção de um pipeline completo de ML, desde a análise dos dados até a avaliação crítica dos modelos.

---

## 📌 Objetivo

Desenvolver e avaliar modelos de Machine Learning capazes de classificar tráfego de rede como **benigno** ou **malicioso**, explorando técnicas de análise de dados, feature engineering e comparação de algoritmos.

---

## 📊 Dataset

* **Fonte:** CICIDS2017 (Canadian Institute for Cybersecurity)
* **Tipo:** Dados de tráfego de rede com múltiplas features estatísticas
* **Acesso:** Dataset público carregado via Hugging Face (`datasets`), utilizando streaming para lidar com o grande volume de dados

**Observação:** O CICIDS2017 é conhecido por conter features altamente discriminativas, o que pode resultar em métricas elevadas.

---

## 🛠️ Pipeline do Projeto

O projeto foi estruturado em notebooks independentes, garantindo reprodutibilidade:

1. **Análise Exploratória de Dados (EDA)**

   * Inspeção das features
   * Distribuição das classes
   * Identificação de inconsistências nos dados

2. **Feature Engineering**

   * Padronização dos nomes das colunas
   * Tratamento de valores infinitos e ausentes
   * Criação da variável alvo (`target`)
   * Normalização das features (quando aplicável)

3. **Modelagem e Avaliação**

   * Treinamento de modelos supervisionados
   * Comparação de desempenho com métricas adequadas
   * Análise de falsos positivos e falsos negativos

---

## 🤖 Modelos Utilizados

* **Logistic Regression** (baseline)
* **Random Forest Classifier**

A Logistic Regression foi utilizada como modelo de referência, enquanto o Random Forest apresentou melhor controle de falsos positivos, característica relevante em cenários de cibersegurança.

---

## 📈 Métricas de Avaliação

Os modelos foram avaliados utilizando:

* Precision
* Recall
* F1-score
* Matriz de confusão

Em problemas de detecção de intrusão, foi dada atenção especial ao **recall da classe de ataque**, devido ao impacto de falsos negativos.

---

## ⚠️ Limitações e Trabalhos Futuros

* Possível viés do dataset, resultando em métricas elevadas
* Avaliação restrita a um subconjunto dos dados

Trabalhos futuros podem incluir:

* Validação temporal (treino/teste por dia)
* Testes com outros datasets de cibersegurança
* Exploração de técnicas de detecção de anomalias

---

## 📦 Dependências

As principais bibliotecas utilizadas neste projeto estão listadas no arquivo `requirements.txt`.

---

## 🎯 Considerações Finais

Este projeto foi desenvolvido com foco em **aprendizado prático e consolidação de conceitos de Machine Learning**, aplicados a um problema real de cibersegurança, servindo como material de estudo e portfólio técnico.
