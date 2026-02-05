# Streamlit — Aplicações Web de IA 

Este repositório reúne os **projetos e exemplos práticos** do curso **“Streamlit: Aplicações Web de IA”**, com várias mini-aplicações em Streamlit cobrindo **Machine Learning**, **Séries Temporais**, **Estatística**, **Recomendação**, **Otimização** e **IA Generativa**.

---

## ✅ O que você vai encontrar aqui

Cada pasta é um exemplo independente (com seu próprio `config.toml` do Streamlit), incluindo datasets `.csv` quando necessário.

Principais temas:

- Regressão linear (previsão de custo)
- Classificação (qualidade de veículos)
- Séries temporais (previsão + decomposição)
- Probabilidade (Poisson) para falhas
- Teste de normalidade
- Recomendação por regras de associação (Apriori)
- Benchmark de modelos de séries temporais
- Análise exploratória com Plotly
- Otimização com algoritmo genético
- IA generativa (Stable Diffusion)
- Visualização de ações (yfinance)
- App completo multipágina (Streamlit Pages)

---

## 🗂️ Estrutura do repositório

```text
.
├─ requirements.txt
├─ 3.Franquia/
│  ├─ reglin.py
│  └─ .streamlit/config.toml
├─ 4.QualidadeVeiculos/
│  ├─ carros.py
│  └─ .streamlit/config.toml
├─ 5.Proleite/
│  ├─ milk.py
│  ├─ monthly-milk-production-pounds-p.csv
│  └─ .streamlit/config.toml
├─ 6.FalhaEquipamento/
│  ├─ equipamento.py
│  └─ .streamlit/config.toml
├─ 7.Normalidades/
│  ├─ normalidade.py
│  ├─ ndata.csv / nndata.csv
│  └─ .streamlit/config.toml
├─ 8.Recomendacao/
│  ├─ mineraregras.py
│  ├─ transacoes.csv
│  └─ .streamlit/config.toml
├─ 9.BenchmarkST/
│  ├─ bmmilk.py
│  ├─ monthly-milk-production-pounds-p.csv
│  └─ .streamlit/config.toml
├─ 10.Exploratoria/
│  ├─ exploratoria.py
│  ├─ dados.csv
│  └─ .streamlit/config.toml
├─ 11.OtimizaCarga/
│  ├─ otimizacarga.py
│  ├─ Itens.csv
│  └─ .streamlit/config.toml
├─ 12.Generativa/
│  ├─ genai.py
│  └─ .streamlit/config.toml
├─ 13.Acoes/
│  ├─ finance.py
│  └─ .streamlit/config.toml
└─ 14.Appcompleta/
   ├─ app.py
   ├─ dados.csv
   ├─ pages/
   │  ├─ 01_🗒️_listagem.py
   │  ├─ 02_🔭_resumo.py
   │  ├─ 03_📊_analisedetalhada.py
   │  └─ 04_🏆_maioresvalores.py
   ├─ requirements.txt
   └─ .streamlit/config.toml
```

---

## 🔧 Requisitos

- **Python 3.10+** (recomendado)
- Dependências em `requirements.txt`

> Observação: o projeto **12.Generativa** usa `diffusers` + `torch` e pode exigir mais recursos (GPU/VRAM). Em CPU funciona, mas pode ser bem mais lento.

---

## 🚀 Instalação

### 1) Criar ambiente virtual (recomendado)

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# Linux/Mac
source .venv/bin/activate
```

### 2) Instalar dependências (geral)

```bash
pip install -r requirements.txt
```

> Se você quiser rodar apenas o app completo (pasta `14.Appcompleta`), você também pode instalar as dependências específicas:
>
> ```bash
> pip install -r 14.Appcompleta/requirements.txt
> ```

---

## ▶️ Como executar (exemplos)

A forma padrão é rodar **um exemplo por vez**:

```bash
streamlit run <pasta>/<arquivo.py>
```

### Exemplos rápidos

**Regressão Linear — Franquia**
```bash
streamlit run 3.Franquia/reglin.py
```

**Classificação — Qualidade de Veículos**
```bash
streamlit run 4.QualidadeVeiculos/carros.py
```

**Séries Temporais — Produção de leite**
```bash
streamlit run 5.Proleite/milk.py
```

**Falhas em equipamentos (Poisson)**
```bash
streamlit run 6.FalhaEquipamento/equipamento.py
```

**Teste de Normalidade**
```bash
streamlit run 7.Normalidades/normalidade.py
```

**Recomendação por Regras (Apriori)**
```bash
streamlit run 8.Recomendacao/mineraregras.py
```

**Benchmark de Séries Temporais**
```bash
streamlit run 9.BenchmarkST/bmmilk.py
```

**Análise Exploratória (Plotly)**
```bash
streamlit run 10.Exploratoria/exploratoria.py
```

**Otimização de carga (Algoritmo Genético)**
```bash
streamlit run 11.OtimizaCarga/otimizacarga.py
```

**IA Generativa — Stable Diffusion**
```bash
streamlit run 12.Generativa/genai.py
```

**Visualizador de Ações (yfinance + Plotly)**
```bash
streamlit run 13.Acoes/finance.py
```

---

## 🧩 App Completo (Multipágina)

A pasta `14.Appcompleta` é um exemplo de aplicação mais “real”, com **várias páginas** (Streamlit Pages) para **análise exploratória de despesas**:

- Listagem (AgGrid)
- Resumo
- Distribuição
- Maiores valores

Para rodar:

```bash
streamlit run 14.Appcompleta/app.py
```

---

## 📝 Descrição dos exemplos

- **3.Franquia — `reglin.py`**: regressão linear para estimar custo inicial com base em um valor anual.
- **4.QualidadeVeiculos — `carros.py`**: classificação usando pré-processamento (OrdinalEncoder) + Naive Bayes categórico.
- **5.Proleite — `milk.py`**: séries temporais com decomposição sazonal e modelo SARIMAX.
- **6.FalhaEquipamento — `equipamento.py`**: cálculo/visualização de probabilidade de falhas usando distribuição de Poisson.
- **7.Normalidades — `normalidade.py`**: testes estatísticos e gráficos para avaliar normalidade.
- **8.Recomendacao — `mineraregras.py`**: mineração de regras de associação com Apriori + métricas de regras.
- **9.BenchmarkST — `bmmilk.py`**: comparação de modelos (ex.: Holt/ETS/ARIMA) para previsão em séries temporais.
- **10.Exploratoria — `exploratoria.py`**: análise exploratória e visualizações com Plotly.
- **11.OtimizaCarga — `otimizacarga.py`**: otimização com algoritmo genético (seleção de itens/carga).
- **12.Generativa — `genai.py`**: geração de imagens com Stable Diffusion via Diffusers.
- **13.Acoes — `finance.py`**: consulta e visualização de ativos/ações com yfinance.
- **14.Appcompleta**: app multipágina para análise exploratória (exemplo completo).

---

## 🔒 Observações importantes

- Alguns exemplos baixam recursos (ex.: modelos) na primeira execução.
- Para IA generativa, considere rodar com GPU se possível.
- Se estiver no Windows e tiver erro com pacotes científicos, atualize `pip`/`setuptools` e tente novamente:
  ```bash
  python -m pip install --upgrade pip setuptools wheel
  ```

---

## 📄 Licença

Defina a licença que preferir (MIT, Apache-2.0 etc.).  
Se você pretende disponibilizar publicamente, recomendo adicionar um arquivo `LICENSE`.

---

## 📬 Autor

**Fernando Amaral**  
Plataforma: **EIA.ai**
