# latex for mac
 MacへのLatexインストールの仕方
- homebrewのインストール
  ```
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
  ```

- brewのアップデート（インストールから始まった人は飛ばしてもいい）。
  ```
  brew update && brew upgrade && brew cleanup
  ```
- latex のインストール(時間かかる)
  ```
  brew install mactex-no-gui
  ```
- Pathの設定(何も出なかったら正常)
  ```
  export PATH=$PATH:/usr/local/texlive/2023/bin/universal-darwin
  ```
- latex liveのアップデート
  ```
  sudo tlmgr update --self --all
  ```
- .latexmkrcをユーザー直下にコピー(これ重要)
- VSCodeのインストール
- VSCodeの拡張機能 "Latex Workshop"をインストール
- VSCodeのsetting.jsonを開く
  [左下の歯車マーク]→[設定]→[右上のファイルのようなマーク]
- その内容を付属のsetting.jsonとコピペで入れ替え
- インストール完了

# Latexの実行
- 付属のsample.texを"command + C"で保存
- outフォルダーにsample.pdfがあれば成功
  
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