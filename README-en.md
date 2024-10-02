# Neural Network Drawing Package (TikZ)

[ja](./README.md)

## Usage

Load the `tikz-nn.sty` package in the preamble:

```latex
\usepackage{tikz-nn}
```

### 1. Fully Connected Neural Network `\fcnn`

```latex
\fcnn[hidden layers]{input}{hidden}{output}
```

**hidden layers**: Number of hidden layers (optional, default: 3)  
**input**: Number of input nodes (required)  
**hidden**: Number of nodes in each hidden layer (required)  
**output**: Number of output nodes (required)

> [!TIP]
> Use `\fcnn` to display labels and `\fcnn*` to hide labels.

At present, there is no scaling option, so please adjust as needed. Additionally, the number of nodes is the same across all hidden layers.

#### Example Usage of `\fcnn`

```latex
\documentclass{ltjsarticle}
\usepackage{float}
\usepackage{tikz-nn}
\pagestyle{empty}

\begin{document}
\begin{figure}[H]
  \fcnn{3}{6}{4}
  \caption{Version with labels.}
\end{figure}
\begin{figure}[H]
  \fcnn*[4]{3}{2}{4}
  \caption{Version without labels.}
\end{figure}
\end{document}
```

### 2. Recurrent Neural Network `\rnn`

```latex
\rnn[hidden layers]{input}{hidden}{output}
```

**hidden layers**: Number of hidden layers (optional, default: 2)  
**input**: Number of input nodes (required)  
**hidden**: Number of nodes in each hidden layer (required)  
**output**: Number of output nodes (required)

> [!TIP]
> Use `\rnn` to display labels and `\rnn*` to hide labels.

Like `\fcnn`, there is no scaling option at this time, so please adjust accordingly. Additionally, the number of nodes is the same across all hidden layers.

#### Example Usage of `\rnn`

```latex
\documentclass{ltjsarticle}
\usepackage{float}
\usepackage{tikz-nn}
\pagestyle{empty}

\begin{document}
\begin{figure}[H]
  \rnn{3}{4}{3}
  \caption{ラベル表示 Ver.}
\end{figure}
\begin{figure}[H]
  \rnn*[1]{3}{5}{2}
  \caption{ラベル非表示 Ver.}
\end{figure}
\end{document}
```

![sample](./sample-rnn.png)

### 3. Autoencoder `\ae`

```latex
\ae[style]{input/output}{hidden}
```

**style**: Type of hidden layers [full/short] (optional, default: short)  
**input/output**: Number of input/output nodes (required)  
**hidden**: Number of nodes in the hidden (latent vector) layer (required)

> [!TIP]
> Use `\ae` to display labels and `\ae*` to hide labels.

Like `\fcnn`, there is no scaling option at this time, so please adjust accordingly.

#### Example Usage of `\ae`

```latex
\documentclass{ltjsarticle}
\usepackage{float}
\usepackage{tikz-nn}
\pagestyle{empty}

\begin{document}
\begin{figure}[H]
  \ae{4}{2}
  \caption{Short version.}
\end{figure}
\begin{figure}[H]
  \ae[full]{4}{2}
  \caption{Full version.}
\end{figure}
\end{document}
```

## 4. Other Neural Networks

In progress...
