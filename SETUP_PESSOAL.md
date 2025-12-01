# 🚀 Guia de Setup Pessoal - Sistema de Predição de Obesidade

Este arquivo contém instruções passo a passo para configurar o projeto em sua própria conta e ambiente.

---

## 📋 Pré-requisitos

- **Python 3.8+** instalado em sua máquina
- **Git** instalado
- **Conta no GitHub** (opcional, mas recomendado para versionamento)
- **Conta no Streamlit Community Cloud** (para deploy público)

---

## 🔧 Instalação Local

### 1. Clone o Repositório

```bash
# Clone o repositório para sua máquina
git clone https://github.com/gustmacena/predicao-obesidade.git
cd predicao-obesidade
```

### 2. Crie um Ambiente Virtual

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Instale as Dependências

```bash
pip install -r requirements.txt
```

---

## 🏃 Executando Localmente

### Opção 1: Aplicação de Predição

```bash
streamlit run app.py
```

A aplicação abrirá em `http://localhost:8501`

### Opção 2: Painel Analítico

```bash
streamlit run app_dashboard.py
```

---

## 🌐 Deploy no Streamlit Community Cloud

### Passo 1: Prepare seu Repositório GitHub

```bash
# Inicialize um repositório Git (se não tiver)
git init
git add .
git commit -m "Initial commit: Sistema de Predição de Obesidade"

# Crie um repositório no GitHub e faça push
git remote add origin https://github.com/SEU_USUARIO/seu-repo-name.git
git branch -M main
git push -u origin main
```

### Passo 2: Deploy no Streamlit Cloud

1. Acesse [Streamlit Cloud](https://streamlit.io/cloud)
2. Clique em **"New app"**
3. Selecione seu repositório GitHub
4. Configure:
   - **Repository:** seu-usuario/seu-repo-name
   - **Branch:** main
   - **Main file path:** app.py (ou app_dashboard.py)
5. Clique em **"Deploy"**

### Passo 3: Compartilhe os Links

Após o deploy, você receberá URLs públicas como:
- Predição: `https://seu-usuario-predicao.streamlit.app/`
- Painel: `https://seu-usuario-painel.streamlit.app/`

---

## 📁 Estrutura do Projeto

```
seu_projeto_streamlit/
├── app.py                      # Aplicação de Predição
├── app_dashboard.py            # Painel Analítico
├── ml_pipeline_obesity.py      # Script de Treinamento
├── Obesity.csv                 # Dataset
├── obesity_pipeline.pkl        # Modelo Treinado
├── requirements.txt            # Dependências
├── .streamlit/
│   └── config.toml            # Configurações do Streamlit
├── README.md                   # Documentação Original
└── SETUP_PESSOAL.md           # Este arquivo
```

---

## 🔧 Personalizações Recomendadas

### 1. Alterar Cores e Tema

Edite `.streamlit/config.toml`:

```toml
[theme]
primaryColor = "#3182CE"
backgroundColor = "#FFFFFF"
secondaryBackgroundColor = "#F5F7FA"
textColor = "#1A202C"
font = "sans serif"
```

### 2. Adicionar Logo ou Branding

Modifique `app.py` e `app_dashboard.py` para incluir:

```python
st.set_page_config(
    page_title="Seu Hospital - Predição de Obesidade",
    page_icon="🏥",
    layout="wide"
)
```

### 3. Integrar com Banco de Dados

Se desejar persistir dados de pacientes, adicione uma integração com:
- **SQLite** (local)
- **PostgreSQL** (cloud)
- **Firebase** (serverless)

---

## 🐛 Troubleshooting

### Erro: "ModuleNotFoundError: No module named 'streamlit'"

```bash
pip install streamlit --upgrade
```

### Erro: "Obesity.csv not found"

Certifique-se de que o arquivo `Obesity.csv` está no mesmo diretório que `app.py`.

### Erro ao fazer Deploy no Streamlit Cloud

1. Verifique se `requirements.txt` está correto
2. Certifique-se de que o arquivo `Obesity.csv` está no repositório
3. Verifique se o arquivo `obesity_pipeline.pkl` está no repositório

---

## 📊 Dados do Modelo

- **Acurácia:** 88%
- **Algoritmo:** Gradient Boosting Classifier
- **Features:** 17 atributos (comportamentais, físicos e históricos)
- **Classes:** 7 níveis de peso (Peso Insuficiente até Obesidade Tipo III)

---

## 📞 Suporte

Para dúvidas ou problemas:

1. Consulte a [Documentação do Streamlit](https://docs.streamlit.io/)
2. Verifique o [Repositório Original](https://github.com/gustmacena/predicao-obesidade)
3. Abra uma issue no seu repositório GitHub

---

## 📝 Próximas Etapas

1. ✅ Clonar o repositório
2. ✅ Instalar dependências
3. ✅ Testar localmente
4. ✅ Deploy no Streamlit Cloud
5. ✅ Compartilhar links com a equipe
6. 🔄 Monitorar e melhorar o modelo

---

**Boa sorte com seu projeto! 🎉**

Tech Challenge - FIAP Pós-Tech | Data Analytics
