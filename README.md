# NPL Sentinel

![NPL Sentinel Banner](./images/sentinel_banner.png)

## Análise de Sentimento em Avaliações de Produtos

### Sobre o Projeto

O objetivo do projeto é implementar Análise de Sentimentos em Avaliações de Produtos submetidas por usuários.

### Especificações

1. **Coleta de Dados:**

   - Dataset: Avaliações dos usuários (texto e nota) para um produto selecionado.
   - Produto Selecionado: Smartphone

2. **Pré-processamento:**

   - Limpeza dos textos (remoção de stopwords, pontuação, normalização, etc.).
   - Conversão das notas em rótulos de sentimento (positivo, negativo, neutro).

3. **Treinamento de Classificadores:**

   - **SVM + Bag-of-Words (BoW):** Classificador SVM utilizando representações BoW.
   - **SVM + Embeddings:** Classificador SVM utilizando embeddings de palavras.
   - **BERT:** Modelo BERT treinado para classificação de sentimento.

4. **In-Context Learning:**

   - **OpenAI GPT-4o:** LLM da OpenAI utilizando Modelo GPT-4o para a classificação de sentimento.
   - **Google Gemini 1.5:** LLM do Google utilizando Modelo Gemini 1.5 para a classificação de sentimento.

5. **Apresentação:**
   - Resultados (F1 e acurácia) e análises em slides.
   - Vídeo de Apresentação com duração máxima de 15 minutos.
