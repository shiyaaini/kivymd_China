# KivyMD [2.0.0](https://kivymd.readthedocs.io/en/latest/changelog/index.html)

<img align="right" height="256" src="https://github.com/kivymd/internal/raw/main/logo/kivymd_logo_blue.png"/>

KivyMD 是一组符合 Material Design 规范的组件库，可与 [Kivy](http://kivy.org) 框架一起使用，用于构建跨平台、支持触摸的图形应用。

本项目的目标是在不牺牲易用性的前提下，尽可能贴近 Google 的 [Material Design 规范](https://material.io/design/introduction/)。该库是 [KivyMD 项目](https://gitlab.com/kivymd/KivyMD) 的一个分支。我们延续并强化了它，将项目提升到了新的水平。

欢迎加入项目！只需 fork 项目，创建分支并在你的更改准备就绪后提交 Pull Request。如果需要进一步修改，我们会通过 PR 评论指导你完成所需步骤，或在必要时请求对你的仓库的访问权限以直接提交更改。

如果你希望成为项目开发者（无需 fork 即可在主仓库创建分支，便于协作），请先确保至少有一个 PR 被合并，然后提出申请。如果你为项目持续贡献，我们也可能主动邀请你担任该角色。

[![PyPI version](https://img.shields.io/pypi/v/kivymd.svg)](https://pypi.org/project/kivymd)
[![Supported Python versions](https://img.shields.io/pypi/pyversions/kivymd.svg)](#Installation)
[![Downloads](https://pepy.tech/badge/kivymd)](https://pepy.tech/project/kivymd)
[![Code style: Black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

[![Discord](https://img.shields.io/discord/566880874789076992?logo=discord)](https://discord.gg/wu3qBST)
[![Twitter](https://img.shields.io/twitter/follow/KivyMD?label=follow&logo=twitter&style=flat&color=brightgreen)](https://twitter.com/KivyMD)
[![YouTube](https://img.shields.io/static/v1?label=subscribe&logo=youtube&logoColor=ff0000&color=brightgreen&message=5k)](https://www.youtube.com/c/KivyMD)
[![Habr](https://img.shields.io/static/v1?label=habr&message=ru&logo=habr&color=brightgreen)](https://habr.com/ru/users/kivymd/posts)
[![StackOverflow](https://img.shields.io/static/v1?label=stackoverflow%20tag&logo=stackoverflow&logoColor=fe7a16&color=brightgreen&message=kivymd)](https://stackoverflow.com/tags/kivymd)
[![Open Collective](https://img.shields.io/opencollective/all/kivymd?label=financial%20contributors&logo=open-collective)](https://opencollective.com/kivymd)

[![覆盖率状态](https://coveralls.io/repos/github/kivymd/KivyMD/badge.svg)](https://coveralls.io/github/kivymd/KivyMD)
[![构建工作流](https://github.com/kivymd/KivyMD/workflows/Build/badge.svg?branch=master)](https://github.com/kivymd/KivyMD/actions?query=workflow%3ABuild)
[![测试工作流](https://github.com/kivymd/KivyMD/workflows/Test/badge.svg?branch=master)](https://github.com/kivymd/KivyMD/actions?query=workflow%3ATest)
[![文档状态](https://readthedocs.org/projects/kivymd/badge/?version=latest)](https://kivymd.readthedocs.io)
[![仓库大小](https://img.shields.io/github/repo-size/kivymd/kivymd.svg)](https://github.com/kivymd/KivyMD)

<a id="Installation"></a>
<a id="installation"></a>
## 安装

```bash
pip install kivymd==2.0.0
```

### 依赖项：

- [Kivy](https://github.com/kivy/kivy) >= 2.3.0（[安装说明](https://kivy.org/doc/stable/gettingstarted/installation.html)）
- [Python 3.7+](https://www.python.org/)
- [Pillow](https://github.com/python-pillow/Pillow/)
- [MaterialColor](https://github.com/T-Dynamos/materialyoucolor-python)
- [asynckivy](https://github.com/asyncgui/asynckivy)

### 如何安装

上方的命令（见 [此处](#installation)）将从 [PyPI](https://pypi.org/project/kivymd) 安装 KivyMD 的最新发行版。

如果你希望从 [master](https://github.com/kivymd/KivyMD/tree/master/) 分支安装开发版，请指定 zip 压缩包链接：

```bash
pip install https://github.com/shiyaaini/kivymd_China/archive/master.zip
```

**提示**：将 `master.zip` 替换为 `<commit hash>.zip`（例如 `51b8ef0.zip`）即可安装指定提交的版本。

你也可以从源码手动安装。克隆项目并执行 pip：

```bash
git clone https://github.com/shiyaaini/kivymd_China.git --depth 1
cd KivyMD
pip install .
```

**加速提示**：如果不需要完整的提交历史（约 1.14 GiB），可以使用浅克隆（`git clone https://github.com/kivymd/KivyMD.git --depth 1`）以节省时间；若需要完整历史，请去掉 `--depth 1`。

### 如何与 [Buildozer](https://github.com/kivy/buildozer) 一起使用

```ini
requirements = python3,
    kivy,
    https://github.com/shiyaaini/kivymd_China/archive/master.zip,
    materialyoucolor,
    exceptiongroup,
    asyncgui,
    asynckivy,
    android
```

这将从 [PyPI](https://pypi.org/project/kivymd) 下载 KivyMD 的最新发行版。

如果你想使用来自 [master](https://github.com/kivymd/KivyMD/tree/master/) 分支的开发版，请指定 zip 压缩包链接：

```ini
requirements = kivy, https://github.com/kivymd/KivyMD/archive/master.zip
```

若更新了版本，构建前别忘了执行 `buildozer android clean` 或删除 `.buildozer` 目录（Buildozer 不会自动更新已下载的包）。

<a id="On-Linux"></a>
#### 在 Linux 上

- 直接使用 Buildozer（[安装方法](https://github.com/kivy/buildozer#installing-buildozer-with-target-python-3-default)）或通过 [Docker](https://github.com/kivy/buildozer/blob/master/Dockerfile)。

#### 在 Windows 10 上

- 安装 [Ubuntu WSL](https://ubuntu.com/wsl) 并按照[Linux 步骤](#On-Linux)进行。

#### 通过 GitHub Actions 自动构建

- 使用 [ArtemSBulgakov/buildozer-action@v1](https://github.com/ArtemSBulgakov/buildozer-action) 在 push 或 PR 时自动构建你的包。
- 参见[完整工作流示例](https://github.com/ArtemSBulgakov/buildozer-action#full-workflow)。

### 如何与 [kivy-ios](https://github.com/kivy/kivy-ios) 一起使用

```bash
toolchain build python3 kivy pillow
toolchain pip install --no-deps kivymd
```

## 文档

- 文档：https://kivymd.readthedocs.io
- 含 KivyMD 组件示例的 Wiki：https://github.com/kivymd/KivyMD/wiki




## 支持

如果你需要帮助或有任何问题，可以通过以下渠道寻求支持：

- **Discord 服务器：** https://discord.gg/wu3qBST（英语 #support，俄语 #ru-support）
- **StackOverflow 标签：** [kivymd](https://stackoverflow.com/tags/kivymd)
- **邮箱：** KivyMD-library@yandex.com

## 设置

#### [在 PyCharm/Intellij IDEA 中为 Kivy/KivyMD .kv 文件提供语法高亮与自动补全](https://github.com/noembryo/KV4Jetbrains)



## 贡献

我们始终欢迎你的[缺陷报告](https://github.com/kivymd/KivyMD/issues/new?template=bug_report.md)、[功能请求](https://github.com/kivymd/KivyMD/issues/new?template=feature_request.md)和 [Pull Request](https://github.com/kivymd/KivyMD/pulls)！
请查看 [CONTRIBUTING.md](https://github.com/kivymd/.github/blob/master/.github/CONTRIBUTING.md)，欢迎一起改进 KivyMD。

### 搭建开发环境

我们推荐使用 PyCharm 来参与 KivyMD 的开发。在你的虚拟环境中安装 [Kivy](https://kivy.org/doc/stable/gettingstarted/installation.html) 和开发依赖：

```bash
pip install -e .[dev,docs]
pre-commit install
```

格式化所有文件并运行测试：

```bash
pre-commit run --all-files
pytest kivymd/tests --timeout=600 --cov=kivymd --cov-report=term
```

pre-commit 将使用 Black 格式化修改过的文件，并用 isort 排序导入。


