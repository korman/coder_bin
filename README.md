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

### 12. lsd

lsd是一个基于 Rust 语言编写的 ls 命令替代品，增加了颜色、图标、树视图、更多格式选项等。可以在 Archlinux、Fedora、macOS、FreeBSD、Windows、Android、Ubuntu、Debian 等多种操作系统上安装。

简单使用

    ```bash
    lsd <path>

    # 例如
    lsd ./xxx
    ```

### 13. fd

fd是一个简单、快速且用户友好的查找工具，类似于find。但是真的比find好用多了。

简单使用

    ```bash
    # 简单使用 假设你想找到你的一个旧脚本（它名字包含 netflix）

    > fd netfl
    Software/python/imdb-ratings/netflix-details.py

    # 搜索模式被当作一个正则表达式来处理。这里，我们搜索以 x 开头、以 rc 结尾的条目：
    > fd '^x.*rc$'
    X11/xinit/xinitrc
    X11/xinit/xserverrc

    # 如果我们想搜索一个特定的目录，可以把它作为 fd 的第二个参数：
    > fd passwd /etc
    /etc/default/passwd
    /etc/pam.d/passwd
    /etc/passwd

    # 列出所有文件，递归
    > fd
    testenv
    testenv/mod.rs
    tests.rs

    # 如果你想使用这个功能来列出一个给定目录中的所有文件，你必须使用一个全包模式，如 . 或 ^
    > fd . fd/tests/
    testenv
    testenv/mod.rs
    tests.rs

    # 搜索一个特定的文件扩展名
    > cd fd
    > fd -e md
    CONTRIBUTING.md
    README.md

    # -e 选项可以与搜索模式结合使用：
    > fd -e rs mod
    src/fshelper/mod.rs
    src/lscolors/mod.rs
    tests/testenv/mod.rs

    # 搜索一个特定的文件名
    # 要找到与所提供的搜索模式完全一致的文件，请使用 -g（或 --glob）选项：
    > fd -g libc.so /usr
    /usr/lib32/libc.so
    /usr/lib/libc.so

    # 隐藏和忽略的文件
    > fd pre-commit
    > fd -H pre-commit
    .git/hooks/pre-commit.sample

    # 匹配完整路径
    > fd -p -g '**/.git/config'
    > fd -p '.*/lesson-\d+/[a-z]+.(jpg|png)'
    ```

### 14. deno

deno是一个基于rust的js/ts运行时，可以用来运行js/ts代码。比nodejs更加安全，更加好用。

简单使用

    ```bash
    deno run <file>

    # 例如
    deno run ./xxx.ts
    ```

### 15. dust

dust是一个用来查看磁盘占用的工具，类似于du。这玩意是真好用，推荐使用。

WARNING: 由于rust的版本问题，目前只能在windows上使用。而且需要: VCRUNTIME140.dll

简单使用

    ```bash
    dust <path>

    # 例如
    dust ./xxx
    ```

### 16. lux

Lux是下载网络上视频的命令行工具，类似于youtube-dl。其支持包含抖音，爱奇艺，优酷，b站，腾讯等众多国内外在线视频下载方便快捷。

### 17. topgrade

topgrade是一个用来更新软件的工具，类似于linux的apt-get update。

### 18. go-stress-testing(go-stress-testing-win.exe)

go-stress-testing是一个用来压测网站的工具，类似于linux的ab。

### 19. tgpt(tgpt.exe)

tgpt是命令行使用ChatGPT的工具，可以用来聊天。

### 20. vcpkg

vcpkg是一个用来管理c++库的工具，类似于linux的apt-get。

使用方法：

    ```bash
    # 安装库
    vcpkg install <name>

    # 例如
    vcpkg install boost

    # 查看库
    vcpkg list

    # 卸载库
    vcpkg remove <name>

    # 例如
    vcpkg remove boost
    ```

### 21. gping

gping是一个用来ping的工具，类似于linux的ping。

```bash
$ gping --help
Ping, but with a graph.

Usage: gping [OPTIONS] [HOSTS_OR_COMMANDS]...

Arguments:
  [HOSTS_OR_COMMANDS]...  Hosts or IPs to ping, or commands to run if --cmd is provided. Can use cloud shorthands like aws:eu-west-1.

Options:
      --cmd
          Graph the execution time for a list of commands rather than pinging hosts
  -n, --watch-interval <WATCH_INTERVAL>
          Watch interval seconds (provide partial seconds like '0.5'). Default for ping is 0.2, default for cmd is 0.5.
  -b, --buffer <BUFFER>
          Determines the number of seconds to display in the graph. [default: 30]
  -4
          Resolve ping targets to IPv4 address
  -6
          Resolve ping targets to IPv6 address
  -i, --interface <INTERFACE>
          Interface to use when pinging
  -s, --simple-graphics
          Uses dot characters instead of braille
      --vertical-margin <VERTICAL_MARGIN>
          Vertical margin around the graph (top and bottom) [default: 1]
      --horizontal-margin <HORIZONTAL_MARGIN>
          Horizontal margin around the graph (left and right) [default: 0]
  -c, --color <color>
          Assign color to a graph entry. This option can be defined more than once as a comma separated string, and the order which the colors are provided will be matched against the hosts or commands passed to gping. Hexadecimal RGB color codes are accepted in the form of '#RRGGBB' or the following color names: 'black', 'red', 'green', 'yellow', 'blue', 'magenta','cyan', 'gray', 'dark-gray', 'light-red', 'light-green', 'light-yellow', 'light-blue', 'light-magenta', 'light-cyan', and 'white'
  -h, --help
          Print help information
  -V, --version
          Print version information
      --clear
          Clear the graph from the terminal after closing the program
```

### 22. lazygit

lazygit是一个用来管理git的工具，是界面化的。

### 23. aria2c(v1.37.0)

aria2c是一个用来下载文件的工具，类似于linux的wget。
支持p2p下载，多线程下载，断点续传等。

### 24. protoc(protoc_rust v3.19.4)

protoc是一个用来生成protobuf文件的工具，类似于linux的protoc。
这个是用来生成rust的protobuf文件的。
且本身是由rust编写的。

### 25. tokei(v13.0.0-alpha.0)

Tokei是一个显示代码信息的统计程序

这是使用tokei的基本方法. 这会报告./foo和所有子文件夹代码.

```bash
$ tokei ./foo
```
