# Maratona de Data Science Mackenzie 2025

## 🎯 Objetivo

Desenvolver um modelo de classificação binária para prever a probabilidade de um cliente aderir a um depósito a prazo oferecido por um banco durante uma campanha de marketing.

## 📊 Sobre a Competição

- **Plataforma**: Kaggle
- **Métrica**: ROC AUC
- **Tipo**: Classificação Binária
- **Prazo**: Até 8 de dezembro de 2025
- **Link**: [Kaggle Competition](https://www.kaggle.com/competitions/analise-preditiva-de-comportamento-bancario)

## 📁 Estrutura do Projeto

```
.
├── data/
│   ├── raw/              # Dados originais (train.csv, test.csv)
│   └── processed/        # Dados processados
├── notebooks/
│   ├── 01_eda.ipynb                    # Análise Exploratória
│   ├── 02_feature_engineering.ipynb    # Engenharia de Features
│   └── 03_modeling.ipynb               # Modelagem e Experimentos
├── src/
│   ├── data/
│   │   └── preprocessing.py
│   ├── features/
│   │   └── engineering.py
│   └── models/
│       ├── train.py
│       └── predict.py
├── submissions/          # Arquivos de submissão
├── models/              # Modelos treinados salvos
├── requirements.txt     # Dependências do projeto
└── README.md
```

## 🔧 Instalação

```bash
# Clone o repositório
git clone https://github.com/DesolateElf-dev/maratona-ds-mackenzie-2025.git
cd maratona-ds-mackenzie-2025

# Crie um ambiente virtual
python -m venv venv
source venv/bin/activate  # Linux/Mac
# ou
venv\Scripts\activate  # Windows

# Instale as dependências
pip install -r requirements.txt
```

## 📋 Dataset

### Variáveis Disponíveis

#### Demográficas
- `age`: Idade do cliente
- `job`: Ocupação
- `marital`: Estado civil
- `education`: Nível educacional

#### Financeiras
- `balance`: Saldo médio anual
- `default`: Histórico de inadimplência
- `housing`: Possui financiamento imobiliário
- `loan`: Possui empréstimo pessoal

#### Campanha
- `contact`: Tipo de contato
- `day`: Dia do último contato
- `month`: Mês do último contato
- `duration`: Duração da chamada (segundos)
- `campaign`: Número de contatos na campanha atual
- `pdays`: Dias desde o último contato
- `previous`: Número de contatos em campanhas anteriores
- `poutcome`: Resultado da campanha anterior

#### Target
- `y`: 1 = aderiu ao depósito | 0 = não aderiu

## 🚀 Roadmap

- [ ] **Fase 1: EDA**
  - [ ] Análise de distribuições
  - [ ] Identificação de outliers
  - [ ] Análise de correlações
  - [ ] Verificação de desbalanceamento

- [ ] **Fase 2: Feature Engineering**
  - [ ] Tratamento de valores faltantes
  - [ ] Encoding de variáveis categóricas
  - [ ] Criação de features derivadas
  - [ ] Normalização/Padronização

- [ ] **Fase 3: Modelagem**
  - [ ] Baseline (Logistic Regression)
  - [ ] LightGBM
  - [ ] XGBoost
  - [ ] CatBoost
  - [ ] Ensemble/Stacking

- [ ] **Fase 4: Validação e Tunning**
  - [ ] Stratified K-Fold Cross-Validation
  - [ ] Otimização de hiperparâmetros
  - [ ] Análise de feature importance
  - [ ] SHAP values para explicabilidade

- [ ] **Fase 5: Submissão**
  - [ ] Gerar arquivo de submissão
  - [ ] Validar formato
  - [ ] Compartilhar notebook com professores

## 📈 Estratégia de Modelagem

### Modelos a Testar
1. **Logistic Regression** (baseline)
2. **LightGBM** (modelo principal)
3. **XGBoost**
4. **CatBoost**
5. **Ensemble** (blending/stacking)

### Validação
- Stratified K-Fold (5 folds)
- Métrica de otimização: ROC AUC

### Features Importantes
- `duration` (mais preditiva, mas cuidado com data leakage)
- `poutcome` (resultado de campanhas anteriores)
- `balance` (situação financeira)
- Interações entre features

## ⚠️ Requisitos da Competição

- ✅ Submissão deve conter **probabilidades** (0 a 1), não classes
- ✅ Formato: `id,y`
- ✅ **Obrigatório**: Compartilhar notebook com:
  - Prof. Dr. Murilo Gazzola (usuário: `gazzola`)
  - Prof. MSc. Marco Vallim (usuário: `kitovallim`)

## 🛠️ Tecnologias Utilizadas

- Python 3.9+
- pandas, numpy
- scikit-learn
- LightGBM, XGBoost, CatBoost
- matplotlib, seaborn, plotly
- SHAP (explicabilidade)

## 📝 Licença

Projeto educacional para a Maratona de Data Science Mackenzie 2025.

## 👤 Autor

Desenvolvido para participação na competição Kaggle.
