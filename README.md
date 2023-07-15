# 单可执行文件工具集合

## 介绍(Introduction)

由于在下非常喜欢单文件工具，所以这里存放了收集的一些非常好用好玩的单文件工具集合，
包含了一些常用的工具，方便开发使用。

注意，本项目仅适用于windows系统。

mac系统在另外一个仓库（还未建立）。

## 使用(Usage)

在环境变量中添加本项目的bin目录，即可使用。

## 工具列表(Tools)

### 1. ripgrep(rg)

这是一个交互式命令行工具，可以轻松查找和替换。 它使用进行查找，然后为您提供一个简单的界面来实时查看替换并有条件地替换匹配项。

简单使用
    
    ```bash
    rg <pattern> <path>

    # 例如单个文件搜索
    rg "hello" ./xxx.txt

    # 例如目录搜索
    rg "hello" -g *.txt

    # 例如目录搜索，忽略某些目录
    rg "hello" -g *.txt -g !*.git


    # 递归搜索
    忘了……
    ```

### 2. ninja

ninja是一个快速的小型构建系统，专为速度而设计。 它使用简单的语法来描述生成的文件是如何从输入文件生成的。

简单使用

    ```bash
    ninja -C <build_dir> <target_name>

    # 例如
    ninja -C build hello
    ```

### 3. gitui

gitui是一个交互式的git命令行工具，可以轻松查看git仓库的状态，提交，分支等。
注意，默认按键是非vim风格的，如果不习惯，可以在配置文件中修改。

简单使用

    ```bash
    gitui
    ``` 

### 4. Spotify TUI(spt)

Spotify TUI是一个交互式的Spotify命令行工具，可以轻松查看Spotify的歌单，歌曲，播放等。

简单使用

    ```bash
    我还没研究……
    ```

### 5. neovide

neovide是一个neovim界面版本。

简单使用

    ```bash
    我还没研究……
    ```

### 6. xsv

xsv 是用 Rust 语言编写的命令行工具，用于索引、切分、分析和合并 CSV 文件，命令行使用简单快速以及可组合。

简单使用

    ```bash
    xsv <command> <args>

    # 例如
    xsv select name,age ./xxx.csv
    ```

### 7. screeps-launcher

screeps-launcher是一个screeps的本地服务器，可以用来本地开发screeps。

简单使用

    ```bash
    screeps-launcher
    ```

### 8. meilisearch

meilisearch是一个全文搜索引擎，可以用来搜索文档，代码等。类似Elaticsearch。

### 9. mdbook

mdbook是一个用来生成文档的工具，可以用来生成文档，类似gitbook。

简单使用

    ```bash
    # 初始化项目
    mdbook init <name>

    # 编译项目
    mdbook build

    # 测试项目
    mdbook test

    # 本地预览项目
    mdbook serve
    ```

### 10. alacritty

alacritty是一个快速的终端模拟器，可以用来替代windows的cmd，powershell，git bash等。

个人感觉很不错，推荐使用。

### 11. bat

bat是一个带有语法高亮和Git集成的cat(查看文件)克隆。

简单使用

    ```bash
    bat <file>

    # 例如
    bat ./xxx.txt
    ```