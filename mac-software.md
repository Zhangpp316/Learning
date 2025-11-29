## Mac 装机软件

允许任何来源设置

```bash
# 打开终端
osascript -e 'do shell script "sudo spctl --master-disable" with administrator privileges'
# 输入后按Enter 输入密码
# 进入系统设置-》 隐私与安全性设置--》拉到最低 允许任何源
```



### 1️⃣安装Xcode

1. 打开苹果开发者下载页（无需付费账号，普通 Apple ID 登录即可）
   https://developer.apple.com/download/more/

2. 搜索 **Command Line Tools**，找到对应你 **macOS** 版本的 **dmg**（下最新版即可）。

   

3. 下载完双击 dmg → 双击 pkg → 一路继续，**2 分钟装好**，终端再执行：

   ```bash
   xcode-select -p
   ```

   看到 `/Library/Developer/CommandLineTools` 即成功。

**Question**

1. 为啥要装Xcode？

**macOS 提示“需要 Xcode”其实是“需要 Command Line Tools”，不装就无法编译任何带 C++ 扩展的 Python 包，包括部分机器学习库。**

2. 为啥不直接在终端装？

```bash
xcode-select --install
# 用这个要装几十个小时
```



### 2️⃣ 安装Homebrew

Homebrew 是一个 **macOS 和 Linux** 系统上的 **软件包管理器**，它的主要作用是让你可以方便地安装、更新、卸载各种开源软件和工具，而不需要手动下载、编译或处理依赖关系。

#### Homebrew 作用：
- **安装软件**：比如 `git`、`node`、`python`、`wget` 等，只需一行命令：
  
  ```bash
  brew install git
  ```
- **更新软件**：一键更新所有已安装的软件：
  
  ```bash
  brew upgrade
  ```
- **卸载软件**：干净地移除不需要的软件：
  
  ```bash
  brew uninstall node
  ```
- **管理软件依赖**：自动处理软件之间的依赖关系。
- **安装图形界面软件（通过 Cask）**：
  
  ```bash
  brew install --cask visual-studio-code
  ```

举例：

如果你想在 Mac 上安装 `python`，不需要去官网下载 `.pkg` 安装包，只需终端输入：
```bash
brew install python
```
Homebrew 会自动下载、编译（或拉取二进制）、配置好路径，直接可用。

#### 安装方法：

```python
###直接去清华源镜像网站下载
https://mirrors.tuna.tsinghua.edu.cn/help/homebrew/
```

 3️⃣安装git

git是Git 是一个**分布式版本控制系统**，由 Linus Torvalds（Linux 之父）在 2005 年开发，用于高效管理代码版本、协作开发、追踪文件变更历史。

Git 本身是开源项目，源码托管在 GitHub 上：
🔗 https://github.com/git/git

```bash
# 用 brew 一键安装
brew install git

# 验证git安装
git --version

# Mac自带python3.9x，查看
python3 --V
```



### 3️⃣安装Pycharm 、VScode 、JDK 、IDEA

这里主要讲的不是`brew install xxx` 而是下载破解版

```bash
# 下面是mac破解版的百度网盘链接

通过百度网盘分享的文件：mac
链接:https://pan.baidu.com/s/1M8gWm2oDNOy0DCK-lCiBnQ 
提取码:69a2
复制这段内容打开「百度网盘APP 即可获取」

# 按照上面的教程装就行
sudo xattr -r -d com.apple.quarantine+（空格）+（拖入app）
```





