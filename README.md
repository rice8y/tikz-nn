# ニューラルネットワーク描画パッケージ (Tikz)

## Usage

プリアンブルで `tikz-nn.sty` を読み込む.

```latex
\usepackage{tikz-nn}
```

### 1. 全結合型ニューラルネットワーク `\fcnn`

```latex
\fcnn[hidden layers]{input}{hidden}{output}
```

**hidden layers**: 隠れ層の層数 (option, default: 3)  
**input**: 入力層のノード数 (required)  
**hidden**: 隠れ層のノード数 (required)  
**output**: 出力層のノード数 (required)

> [!TIP]
> `\fcnn` でラベル表示, `\fcnn*` でラベル非表示.

なお, 現時点でスケーリングオプションは無い為, 必要に応じて対処してください. また, 隠れ層の各層におけるノード数は均一です.

#### 例

```latex:sample-fcnn.tex
\documentclass{ltjsarticle}
\usepackage{float}
\usepackage{tikz-nn}
\pagestyle{empty}

\begin{document}
\begin{figure}[H]
  \fcnn{3}{6}{4}
  \caption{ラベル表示Ver.}
\end{figure}
\begin{figure}[H]
  \fcnn*[4]{3}{2}{4}
  \caption{ラベル非表示Ver.}
\end{figure}
\end{document}
```

![sample](sample-fcnn.png)