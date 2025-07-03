<h1>🎬 Smart Movie Review Analyzer</h1>

<p>This project builds a complete movie review analysis system using the IMDB dataset. It performs sentiment classification and extractive summarization using both traditional ML and deep learning models.</p>

<hr>

<h2>📌 Objectives</h2>
<ul>
  <li>Classify IMDB reviews as <strong>positive or negative</strong></li>
  <li>Compare <strong>ANN vs CNN</strong> performance</li>
  <li>Use <strong>Word2Vec</strong> embeddings</li>
  <li>Generate <strong>extractive summaries</strong> using <strong>TextRank</strong></li>
  <li>Visualize important features and evaluate model performance</li>
</ul>

<hr>

<h2>🗃️ Dataset</h2>
<ul>
  <li>Source: <a href="https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews">Kaggle IMDB Dataset</a></li>
  <li>50,000 labeled reviews (balanced)</li>
  <li>Preprocessing: HTML tag removal, lowercase, stopword removal</li>
</ul>

<hr>

<h2>🧠 Models</h2>

<h3>✅ Baseline</h3>
<ul>
  <li><strong>TF-IDF + Logistic Regression</strong> — Accuracy: ~87%</li>
</ul>

<h3>✅ ANN (3-layer neural net + Word2Vec)</h3>
<ul>
  <li>Accuracy: <strong>88.15%</strong></li>
  <li>F1-score: <strong>0.88</strong></li>
  <li><strong>Confusion Matrix:</strong><br>
    <pre>
[[4340  728]
 [ 457 4475]]
    </pre>
  </li>
</ul>

<h3>✅ CNN (1D convolutional + Word2Vec)</h3>
<ul>
  <li>Accuracy: <strong>86.29%</strong></li>
  <li>F1-score: <strong>0.86</strong></li>
  <li><strong>Confusion Matrix:</strong><br>
    <pre>
[[4482  497]
 [ 874 4147]]
    </pre>
  </li>
</ul>

<hr>

<h2>📊 Evaluation Metrics</h2>
<table border="1" cellpadding="5">
  <thead>
    <tr>
      <th>Model</th>
      <th>Accuracy</th>
      <th>Precision</th>
      <th>Recall</th>
      <th>F1-score</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>ANN</td>
      <td>88.15%</td>
      <td>0.88</td>
      <td>0.88</td>
      <td>0.88</td>
    </tr>
    <tr>
      <td>CNN</td>
      <td>86.29%</td>
      <td>0.87</td>
      <td>0.86</td>
      <td>0.86</td>
    </tr>
  </tbody>
</table>

<hr>

<h2>🧾 Word Embeddings</h2>
<ul>
  <li>Used <strong>pretrained Word2Vec</strong></li>
  <li>Document vectors computed by averaging word embeddings</li>
  <li>Enabled semantic similarity for classification & summarization</li>
</ul>

<hr>

<h2>✂️ Text Summarization</h2>
<ul>
  <li>Method: <strong>TextRank</strong> (Extractive Summarization)</li>
  <li>Summarized 200+ word reviews into top 2–3 ranked sentences</li>
  <li>Similarity via <code>cosine similarity</code>, ranking via <code>PageRank</code></li>
</ul>

<blockquote>
  <strong>Example:</strong><br>
  Original Review: (200+ words)<br>
  Summary: “Direction and writing kept me engaged. Cinematography matched the tone.”
</blockquote>

<hr>

<h2>📚 Libraries Used</h2>
<ul>
  <li><code>pandas</code>, <code>numpy</code>, <code>sklearn</code></li>
  <li><code>nltk</code>, <code>gensim</code>, <code>tensorflow</code>, <code>matplotlib</code></li>
  <li><code>networkx</code> for PageRank-based summarization</li>
</ul>

<hr>

<h2>✅ Conclusion</h2>
<ul>
  <li>ANN slightly outperformed CNN for review sentiment classification</li>
  <li>TextRank summarizer worked well for long, structured reviews</li>
  <li>Word embeddings enhanced classification and summarization quality</li>
</ul>

<hr>

<h2>📁 Output</h2>
<ul>
  <li>Summaries saved to <code>summarized_reviews.csv</code></li>
</ul>
