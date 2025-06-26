# 《无刃传说》仓库

-> **[项目企划页面](https://powerforlovegroup.github.io/LegendOfTheVoidBlade/)**

## 关于 MkDocs 的使用

* 请确认你的计算机中安装了Python，建议你安装最新版本。
* 以下所有命令都应在 /docs 目录下使用。

### Linux/MacOS

如果你没有Python虚拟环境，你需要创建一个，请运行：
```
make setup
```

在你完成对文档的修改后，如果你想在本地搭建文档页面以查看你修改后的文档，请运行：
```
make serve
```

在你确认你的修改可行后，如果你想把你的修改应用至 GitHub Pages 中，请运行：
```
make deploy
```

### Windows

如果你没有Python虚拟环境，你需要创建一个，请运行：
```
python -m venv venv
.\venv\Scripts\pip install --upgrade pip
.\venv\Scripts\pip install mkdocs
```

在你完成对文档的修改后，如果你想在本地搭建文档页面以查看你修改后的文档，请运行：
```
.\venv\Scripts\mkdocs serve -a 0.0.0.0:8000
```

在你确认你的修改可行后，如果你想把你的修改应用至 GitHub Pages 中，请运行：
```
.\venv\Scripts\mkdocs gh-deploy --clean
```
