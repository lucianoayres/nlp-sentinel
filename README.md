# NLP-Sentinel

**Análise de Sentimentos em Português usando Deep Learning e LLMs**

Uma solução completa para classificação de sentimentos em avaliações de e-commerce usando técnicas avançadas de Deep Learning e Processamento de Linguagem Natural.

## Documentação e Recursos

- 📝 Relatório Completo: [Markdown](report/project-report.md) | [PDF](report/project-report.pdf)
- 📓 [Jupyter Notebook](notebook/Pos_Deep_Learning_Projeto_NLP_Sentinel_Projeto.ipynb)
- 💻 [Código Fonte](src/pos_deep_learning_projeto_nlp_sentinel_projeto.py)

## Demo Online

Experimente a aplicação em:  
➡️ [Hugging Face Spaces](https://huggingface.co/spaces/layers2024/sentiment-analysis)

## 📊 Resultados Principais

| Modelo              | Acurácia | F1-Score |
|---------------------|----------|----------|
| BERTimbau          | 94.26%   | 94.37%   |
| XLM-RoBERTa        | 93.85%   | 93.94%   |
| DistilBERT         | 93.28%   | 93.37%   |
| SVM + SBERT        | 92.80%   | 92.93%   |
| SVM + USE          | 91.95%   | 92.05%   |

*LLMs (GPT-4, Gemini 1.5) atingiram 100% de acurácia em teste limitado (10 amostras)*

## 🎯 Objetivos

- Implementar e comparar diferentes abordagens de Deep Learning para classificação binária de sentimentos em português
- Avaliar trade-offs entre performance e custo computacional
- Desenvolver uma aplicação web para demonstração em tempo real
- Explorar o potencial de LLMs em zero-shot para análise de sentimentos em português

## 💻 Tecnologias

### Modelos Supervisionados
- **Transformers**
  - BERTimbau (BERT português, ~110M parâmetros)
    - Base: [neuralmind/bert-base-portuguese-cased](https://huggingface.co/neuralmind/bert-base-portuguese-cased)
    - Fine-tuned: [layers2024/bert-sentiment](https://huggingface.co/layers2024/bert-sentiment)
  - XLM-RoBERTa (multilíngue, ~125M parâmetros)
  - DistilBERT (multilíngue leve, ~66M parâmetros)

### Abordagens Híbridas
- **SVM + Embeddings**
  - Universal Sentence Encoder (USE)
  - Sentence-BERT (SBERT)

### LLMs Zero-shot
- OpenAI GPT-4
- Google Gemini 1.5

## 📚 Dataset

- **Origem**: Olist Store (e-commerce brasileiro)
- **Volume**: +100.000 avaliações em português (2016-2018)
- **Classes**:
  - Positivo: 4-5 estrelas (~40k reviews)
  - Negativo: 1-2 estrelas (~20k reviews)
  - *Neutro (3 estrelas) excluído*
- **Split**: 80/10/10 (treino/validação/teste)

## 📱 Aplicação Web

Uma interface web intuitiva foi desenvolvida usando o melhor modelo (BERTimbau):

- **Framework**: Gradio
- **Características**:
  - Interface intuitiva e responsiva
  - Processamento em tempo real
  - Indicador de confiança na classificação
  - Exemplos pré-carregados
- **Repositório**: [sentiment-analysis-app](https://github.com/lucianoayres/sentiment-analysis-app)

## 🔍 Principais Conclusões

1. **Alta Performance**: Todos os modelos transformer superaram 93% de acurácia
2. **Melhor Modelo**: BERTimbau fine-tunado (94.26% acurácia)
3. **Alternativa Eficiente**: SVM + SBERT oferece boa performance com menor custo computacional
4. **Potencial LLMs**: Excelente performance em zero-shot, porém testado em amostra limitada

## 🚀 Como Executar

### Projeto Principal

1. Clone o repositório
```bash
git clone https://github.com/lucianoayres/nlp-sentinel.git
cd nlp-sentinel
```

2. Instale as dependências
```bash
pip install -r requirements.txt
```

### Aplicação Web

1. Clone o repositório da aplicação
```bash
git clone git@github.com:lucianoayres/sentiment-analysis-app.git
cd sentiment-analysis-app
```

2. Execute o script de instalação
```bash
./run.sh
```

3. Execute a aplicação web
```bash
python app.py
```

## 📝 Citação

```bibtex
@article{carvalho2024nlpsentinel,
  title={Análise Comparativa de Técnicas Avançadas de Deep Learning para Classificação de Sentimentos em Avaliações Multidomínio},
  author={Carvalho, Luciano Ayres Farias de},
  institution={Centro de Informática (CIn-UFPE)},
  year={2024}
}
```

## 👤 Autor

**Luciano Ayres Farias de Carvalho**  
Centro de Informática (CIn)  
Universidade Federal de Pernambuco (UFPE)  
Email: lafc@cin.ufpe.br

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---
Desenvolvido como parte do curso de Pós-graduação em Deep Learning no CIn-UFPE.
