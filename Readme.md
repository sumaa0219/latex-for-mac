# latex for mac
- install homebrew
  ```
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
  ```

- brewのアップデート。
  ```
  brew update && brew upgrade && brew cleanup
  ```
 - latex のインストール
  ```
  brew install mactex-no-gui
  ```
 - Pathの設定
  ```
  export PATH=$PATH:/usr/local/texlive/2023/bin/universal-darwin
  ```
 - latex liveのアップデート
  ```
  sudo tlmgr update --self --all
  ```
  
  
 - テンプレート 
  ```
  \documentclass[a4paper,11pt]{jsarticle}


% 数式
\usepackage{amsmath,amsfonts}
\usepackage{bm}
% 画像
\usepackage[dvipdfmx]{graphicx,xcolor}

\usepackage{tikz}
\usetikzlibrary{intersections, calc, arrows.meta}


\begin{document}

\title{}
\author{}
\date{\today}
\maketitle





\end{document}
  ```