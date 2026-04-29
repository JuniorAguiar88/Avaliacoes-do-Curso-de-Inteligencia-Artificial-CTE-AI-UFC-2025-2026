```markdown
# 🤖 Avaliações do Curso de Inteligência Artificial - CTE/AI/UFC

> **Curso:** Inteligência Artificial  
> **Instituição:** Centro de Tecnologia (CTE) - Universidade Federal do Ceará (UFC)  
> **Período:** 2025.2 - 2026.1  
> **Repositório:** Coleção de atividades, exercícios e projetos desenvolvidos durante o curso.

---

## 📋 Sobre o Repositório

Este repositório centraliza as entregas das atividades práticas do curso de **Inteligência Artificial** oferecido pelo CTE-AI/UFC. Aqui você encontrará:

- ✅ Notebooks Jupyter (`.ipynb`) com soluções das atividades
- ✅ Implementações de algoritmos de Machine Learning e Deep Learning
- ✅ Análises exploratórias, pré-processamento e visualização de dados
- ✅ Documentação técnica e relatórios das soluções propostas

> ⚠️ **Atenção:** Este repositório contém material acadêmico. O uso do código para fins de cópia ou plágio é expressamente proibido.

---

## 🗂️ ⚠️ Importante: Datasets e Dados Externos

### 📦 Onde estão os datasets?

Os arquivos de dados (`.csv`, `.xlsx`, `.pkl`, imagens, etc.) **NÃO estão incluídos** neste repositório para:
- Manter o histórico do Git leve e rápido
- Evitar limites de tamanho do GitHub (100MB por arquivo)
- Facilitar o versionamento apenas do código e documentação

### 🔗 Como acessar os datasets?

Todos os datasets utilizados nas atividades estão disponíveis no **Hugging Face Datasets**, organizados por atividade:

```
📌 Em cada notebook (.ipynb), você encontrará no início do código:
   - Uma célula com o link direto para o dataset no Hugging Face
   - O comando `load_dataset()` configurado para baixar automaticamente
   - Instruções de pré-processamento específicas para aquele dado
```

**Exemplo de uso dentro dos notebooks:**
```python
from datasets import load_dataset

# Dataset da Atividade 1 - Classificação de Iris
dataset = load_dataset("jwajr/ufc-ai-atividade1-iris", split="train")

# Dataset da Atividade 2 - Regressão de Demanda
# dataset = load_dataset("jwajr/ufc-ai-atividade2-demanda", split="train")
```

---

## 📁 Estrutura do Projeto

```
📦 Avaliacoes-do-Curso-de-Inteligencia-Artificial-CTE-AI-UFC-2025-2026
 ┣ 📂 notebooks/
 ┃ ┣ 📂 atividade1/          # Tema: Introdução ao ML / Classificação
 ┃ ┃ ┣ 📄 classificacao_iris.ipynb
 ┃ ┃ ┗ 📄 README.md
 ┃ ┣ 📂 atividade2/          # Tema: Regressão / Séries Temporais
 ┃ ┃ ┗ 📄 previsao_demanda.ipynb
 ┃ ┗ 📂 projeto_final/       # Tema: Projeto integrador
 ┃   ┗ 📄 modelo_final.ipynb
 ┣ 📂 datasets/              # ⚠️ Pasta ignorada no Git (use Hugging Face)
 ┣ 📄 .gitignore             # Regras para excluir datasets e arquivos temporários
 ┣ 📄 requirements.txt       # Dependências do projeto (bibliotecas Python)
 ┗ 📄 README.md              # Este arquivo
```

---

## 🚀 Como Executar os Notebooks

### Pré-requisitos
- Python 3.9 ou superior
- Jupyter Notebook / JupyterLab
- Git
- Conta no Hugging Face (opcional, para datasets privados)

### Instalação das Dependências

```bash
# Clone o repositório
git clone https://github.com/JuniorAguiar88/Avaliacoes-do-Curso-de-Inteligencia-Artificial-CTE-AI-UFC-2025-2026.git
cd Avaliacoes-do-Curso-de-Inteligencia-Artificial-CTE-AI-UFC-2025-2026

# Crie um ambiente virtual (recomendado)
python -m venv venv
# Windows:
venv\Scripts\activate
# Linux/Mac:
source venv/bin/activate

# Instale as bibliotecas necessárias (incluindo Hugging Face)
pip install -r requirements.txt
```

### Autenticação no Hugging Face (se necessário)
```bash
# Para datasets privados ou para evitar rate limits:
# 1. Crie um token em: https://huggingface.co/settings/tokens
# 2. Faça login via terminal:
huggingface-cli login
# 3. Cole seu token quando solicitado
```

### Executando um Notebook
```bash
# Inicie o Jupyter
jupyter notebook

# Ou execute diretamente via terminal (sem interface):
jupyter nbconvert --to notebook --execute notebooks/atividade1/classificacao_iris.ipynb
```

---

## 📦 Dependências Principais

As bibliotecas utilizadas estão listadas no arquivo `requirements.txt`. Principais pacotes:

| Pacote | Versão Mínima | Finalidade |
|--------|--------------|------------|
| `numpy` | 1.24+ | Computação numérica |
| `pandas` | 2.0+ | Manipulação de dados |
| `scikit-learn` | 1.3+ | Algoritmos de ML clássicos |
| `matplotlib` / `seaborn` | 3.7+ / 0.12+ | Visualização de dados |
| `jupyter` | 1.0+ | Ambiente interativo |
| `datasets` | 2.14+ | Carregamento de datasets do Hugging Face |
| `tensorflow` / `torch` | *opcional* | Redes neurais (quando aplicável) |

Para instalar tudo de uma vez:
```bash
pip install numpy pandas scikit-learn matplotlib seaborn jupyter datasets
```

---

## 📚 Atividades Desenvolvidas

| Atividade | Tema | Técnicas Utilizadas | Dataset (Hugging Face) | Status |
|-----------|------|---------------------|------------------------|--------|
| `atividade1` | Classificação Supervisionada | Logistic Regression, KNN, Decision Trees | `jwajr/ufc-ai-atividade1-iris` | ✅ Concluído |
| `atividade2` | Regressão e Validação | Linear Regression, Cross-Validation, MSE/R² | `jwajr/ufc-ai-atividade2-demanda` | ✅ Concluído |
| `atividade3` | Processamento de Linguagem Natural | TF-IDF, Naive Bayes, BERT (opcional) | `jwajr/ufc-ai-atividade3-nlp` | ✅ Concluído |
| **`projeto_final_cv`** | **Classificação de Espécies de Peixes** | **YOLOv8-cls, Transfer Learning, OpenCV, Data Augmentation** | **`jwajr/ufc-cv-fish-classification`** | ✅ **Concluído** |

---

## ⚙️ Configurações e Boas Práticas

### 🧹 Notebooks Leves
- Outputs de células foram limpos com `nbstripout` para reduzir o tamanho dos arquivos
- Gráficos são gerados dinamicamente na execução
- Dados são carregados via `datasets.load_dataset()` do Hugging Face

### 🔒 `.gitignore` Configurado
Arquivos e pastas automaticamente ignorados:
```gitignore
# Dados e arquivos grandes
*.csv
*.xlsx
*.zip
*.tar.gz
*.pkl
*.h5
*.parquet
data/
datasets/
__pycache__/
.ipynb_checkpoints/
*.log
env/
venv/
.DS_Store
```

---

## 🤝 Contribuições

Este é um repositório acadêmico pessoal. Caso você seja colaborador do curso:

1. Crie uma branch para sua feature: `git checkout -b feature/minha-atividade`
2. Adicione suas alterações: `git add notebooks/minha_pasta/`
3. Commit descritivo: `git commit -m "feat: adiciona solução da atividade X"`
4. Push e pull request: `git push origin feature/minha-atividade`

---

## 📄 Licença e Uso Acadêmico

```
Este material foi desenvolvido para fins educacionais no âmbito do curso de 
Inteligência Artificial do CTE/UFC.

✅ Permitido: 
   - Estudo, consulta e referência para aprendizado
   - Adaptação para fins didáticos com devida atribuição
   - Download e uso dos datasets via Hugging Face conforme licença de cada um

❌ Não permitido:
   - Cópia integral ou parcial para submissão como trabalho próprio (plágio)
   - Uso comercial sem autorização prévia
   - Redistribuição dos datasets fora do Hugging Face sem permissão

Em caso de uso, cite a fonte original:
> Aguiar, J. (2025). Avaliações do Curso de IA - CTE/UFC. GitHub. 
> https://github.com/JuniorAguiar88/Avaliacoes-do-Curso-de-Inteligencia-Artificial-CTE-AI-UFC-2025-2026
```

---

## 📬 Contato

| Autor | GitHub | LinkedIn | E-mail | Telefone |
|-------|--------|----------|--------|----------|
| Junior Aguiar | [@JuniorAguiar88](https://github.com/JuniorAguiar88) | [linkedin.com/in/jwajr](https://www.linkedin.com/in/jwajr/) | jwajrr@gmail.com | +55 (92) 99190-2659 |

> 💡 Dúvidas, sugestões ou problemas? 
> - Abra uma **Issue** neste repositório
> - Entre em contato por e-mail ou LinkedIn
> - Consulte a documentação dos datasets no [Hugging Face](https://huggingface.co/datasets/jwajr)

---

<div align="center">

**🎓 CTE-AI/UFC — Inteligência Artificial Aplicada**  
*Desenvolvendo soluções com ética, técnica e inovação.*

[![GitHub](https://img.shields.io/badge/GitHub-Repositório-181717?style=flat&logo=github)](https://github.com/JuniorAguiar88/Avaliacoes-do-Curso-de-Inteligencia-Artificial-CTE-AI-UFC-2025-2026)
[![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=flat&logo=python&logoColor=white)](https://www.python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat&logo=jupyter)](https://jupyter.org)
[![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Datasets-FFD21E?style=flat&logo=huggingface)](https://huggingface.co/datasets/jwajr)

</div>

---
