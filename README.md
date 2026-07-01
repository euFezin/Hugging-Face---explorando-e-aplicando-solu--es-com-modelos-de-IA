# Hugging Face — Explorando e Aplicando Soluções com Modelos de IA

Repositório com notebooks desenvolvidos durante estudos de aplicações práticas com modelos de IA usando a biblioteca Transformers do Hugging Face.

---

## Estrutura

```
hugging-face-modelos-ia/
├── notebooks/
│   ├── hugging_face.ipynb        # Análise de sentimento
│   ├── hugging_face_2.ipynb      # Classificação zero-shot
│   └── hugging_face_3.ipynb      # Remoção de fundo em imagens
└── imagens/
    ├── camera_fotografica.jpg
    ├── serum_labial.jpg
    └── teclado.jpg
```

---

## Notebooks

### 1. Análise de Sentimento (`hugging_face.ipynb`)
Classificação de sentimentos em resenhas de produtos em português e inglês.

**Modelos utilizados:**
- `distilbert-base-uncased-finetuned-sst-2-english` — análise em inglês via Transformers pipeline
- `pysentimiento` — análise em português (POS, NEG, NEU)

**Funcionalidades:**
- Predição de sentimento em resenhas individuais
- Aplicação em massa sobre dataset CSV
- Visualização com gráfico de barras (Plotly)
- Nuvem de palavras por sentimento (WordCloud + NLTK stopwords)

---

### 2. Classificação Zero-Shot (`hugging_face_2.ipynb`)
Classificação de textos em categorias sem necessidade de treinamento prévio.

**Modelos utilizados:**
- `facebook/bart-large-mnli` — classificação zero-shot em inglês
- `knowledgator/comprehend_it-multilingual-t5-base` — classificação multilíngue via liqfit

**Funcionalidades:**
- Classificação de descrições de produtos em categorias customizadas
- Suporte multilíngue (português incluso)
- Aplicação em dataset CSV com categorização automática

> ⚠️ Este notebook requer `transformers==4.41.0` por compatibilidade com o liqfit. A célula de instalação já está configurada.

---

### 3. Remoção de Fundo em Imagens (`hugging_face_3.ipynb`)
Remoção automática de fundo de imagens usando segmentação.

**Modelo utilizado:**
- `briaai/RMBG-1.4` — segmentação e remoção de fundo

**Funcionalidades:**
- Remoção de fundo em imagens via URL e arquivo local
- Interface web interativa com Gradio para uso sem código

---

## Como executar

Todos os notebooks foram desenvolvidos no **Google Colab**. Para executar:

1. Abra o notebook desejado no Colab
2. Execute a célula de instalação de dependências (primeira célula)
3. Faça **Restart session** após a instalação
4. Execute as demais células normalmente

---

## Tecnologias

- Python · Pandas · Plotly · NLTK · WordCloud