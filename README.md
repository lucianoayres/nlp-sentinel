**Projeto:** Implementar Análise de Sentimentos em Avaliações de Produtos

**Especificações:**

1. **Coleta de Dados:**

    - Coletar avaliações dos usuários (texto e nota) para um produto selecionado.

2. **Treinamento de Classificadores:**

    - **SVM + Bag-of-Words (BoW):** Treinar um classificador SVM utilizando representações BoW.
    - **SVM + Embeddings:** Treinar um SVM utilizando embeddings de palavras.
    - **BERT:** Treinar um modelo BERT para classificação de sentimento.

3. **Bônus:**

    - Utilizar **in-context learning** com LLMs para a classificação.

4. **Apresentação:**
    - Reportar resultados (F1 e acurácia) e análises em slides.
    - Produzir um vídeo com duração máxima de 15 minutos.

**Etapas do Projeto:**

1. **Coleta de Dados de Avaliações de Produtos:**

    - Escolher um produto específico.
    - Extrair avaliações (comentários e notas) de fontes como sites de e-commerce.

2. **Pré-processamento:**

    - Limpeza dos textos (remoção de stopwords, pontuação, normalização, etc.).
    - Conversão das notas em rótulos de sentimento (positivo, negativo, neutro).

3. **Treinamento dos Classificadores:**

    - Implementar e treinar os modelos SVM + BoW, SVM + Embeddings e BERT.
    - Ajustar hiperparâmetros e validar modelos.

4. **Avaliação:**

    - Calcular métricas como F1-score e acurácia para cada modelo.
    - Comparar os resultados entre os diferentes métodos.

5. **Bônus (Opcional):**

    - Explorar o uso de LLMs com **in-context learning** para a tarefa de classificação.

6. **Apresentação dos Resultados:**
    - Preparar slides detalhando o processo e resultados.
    - Gravar um vídeo explicativo com até 15 minutos de duração.
