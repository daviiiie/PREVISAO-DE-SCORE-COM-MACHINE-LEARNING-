# Previsão de Score de Crédito com Machine Learning

Projeto de classificação que prevê o score de crédito de clientes de um banco
(**Poor**, **Standard** ou **Good**) a partir do perfil financeiro de cada um.

> Desenvolvido durante a **Jornada Python** (Hashtag Treinamentos), Aula 3:
> *Projeto de Previsão com Machine Learning*.

## Objetivo

Treinar e comparar dois modelos de classificação para identificar, de forma
automática, o score de crédito de um cliente, apoiando a decisão de conceder
crédito.

## Dados

| Arquivo | Descrição |
|---|---|
| `clientes.csv` | 100.000 registros com informações financeiras e o `score_credito` (variável a prever) |
| `novos_clientes.csv` | 3 clientes sem score, usados como teste final do modelo |

Colunas principais: idade, profissão, salário anual, número de contas e
cartões, juros de empréstimo, dias de atraso, dívida total, taxa de uso de
crédito e comportamento de pagamento.

## Etapas do projeto

1. Importação da base com **pandas**
2. Verificação de valores vazios (a base não tinha)
3. Conversão das colunas de texto (`profissao`, `comportamento_pagamento`,
   `mix_credito`) em números com **LabelEncoder**
4. Separação em treino (70%) e teste (30%)
5. Treino de dois modelos: **Random Forest** e **KNN**
6. Comparação por **acurácia**
7. Previsão do score de novos clientes com o melhor modelo

## Resultados

| Modelo | Acurácia (teste) |
|---|---|
| **Random Forest** | ~82% |
| KNN | ~73% |

O Random Forest teve o melhor desempenho e foi usado nos novos clientes, com
previsão: `Poor`, `Standard` e `Standard`.

> A acurácia varia levemente a cada execução, porque a divisão treino/teste é
> aleatória.

## Tecnologias

Python · pandas · scikit-learn · Jupyter Notebook

## Como executar

```bash
# 1. clonar o repositório
git clone https://github.com/SEU-USUARIO/NOME-DO-REPO.git
cd NOME-DO-REPO

# 2. instalar as dependências
pip install pandas scikit-learn jupyter

# 3. abrir o notebook
jupyter notebook inicial.ipynb
```

## Créditos

Intensivão da Jornada Python da Hashtag Treinamentos.
Código: **Davi Freitas**
