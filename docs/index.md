## 使用说明

本模板有两种使用方式，本地编译和Overleaf。

#### Overleaf

Overleaf是一个网页版的LaTeX集成编辑环境，我们已经将模板副本上传至Overleaf，你只需注册一个账号，就能立即开始写作。

#### 本地编译

本地编译需要配置环境，LaTeX和C一样，是一门语言。因此它需要**编译器**和**编辑器**两个组件。

+   编译器取决于你的操作系统，Windows上可以安装MikTex。

+   编辑器推荐VS Code + LaTeX WorkShop插件。

## LaTeX命令

#### 基本格式控制

```latex
\textbf{加粗}
\textit{斜体}
```

#### 多级标题

```latex
\section{一级标题}
\subsection{二级标题}
\subsubsection{三级标题}

\nonumsection{一级标题（无编号）}
```

#### 插入图片

```latex
\begin{figure}[h]
    \centering
    \includegraphics[scale=1.0]{imgs/xxx.png}
    \caption{图片标题}
\end{figure}
```

#### 插入表格

可以使用在线工具[TableGenerator](https://www.tablesgenerator.com/)生成。

#### 插入公式

```latex
\begin{equation}
	a + b = \lambda
\end{equation}
```

#### 插入代码

```latex
\begin{lstlisting}[language=Python]
def add(x, y):
	return x + y
\end{lstlisting}
```

#### 插入附录

```latex
\nonumsection{附录}
\appendixformat
```

#### 引用图表与公式

在要引的图表或公式处使用`\label{标签}`命令，加入标签。例如：

```latex
\begin{equation}
	a + b = \lambda		\label{eq:a+b}
\end{equation}
```

对于图表使用`\ref{标签}`，对公式使用`\eqref{标签}`。

```latex
式\eqref{eq:a+b}

图\ref{标签}
表\ref{标签}
```

#### 引用文献

在百度学术或知网中找到要引的文献，导出bibtex格式，将其粘贴到`references.bib`文件中。例如：

```latex
@article{bib02,		% 第一行是文献名
  title={科学技术报告、学位论文和学术论文的编写格式},
  author={YoviSun.COM, yovisunqq.com},
  journal={郑州航空工业管理学院学报},
  number={2},
  pages={55-56},
  year={1991},
}
```

接着，你可以在`main.tex`文件中对该文献进行引用。

```latex
\cite{bib02}
```

## 开源许可

本项目基于[LPPL-1.3c License](https://github.com/blueloveTH/cucthesis/blob/main/License)开源。