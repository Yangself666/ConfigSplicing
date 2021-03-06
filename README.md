# 项目简介

用来生成 Surge/Clash 配置文件的 `python` 脚本。

# 实现功能

- [x] 支持不同类型的节点订阅链接（Surge、SS）
- [x] 支持同时输入多个节点订阅链接（相同类型或者不同类型）
- [x] 支持自定义规则链接
- [x] 支持为策略组添加节点
- [x] 支持修改策略组名字（有限）
- [x] 支持输出 Surge 或者 Clash 配置文件

# 使用方法

- 下载或者克隆项目后，进入项目文件夹：

  ```bash
  # 例如
  cd ConfigSplicing
  ```

- 安装依赖：

  ```bash
  pip3 install .
  ```
  
- 输入命令：

  ```bash
  # 查看帮助
  cs --help
  
  Usage: cs [OPTIONS] [SUB_LINKS]...
  
    ConfigSplicing
  
  Options:
    -R, --rename            更改策略组名
    -c, --clash             输出Clash配置文件
    -r, --rule TEXT         规则链接（默认为神机规则）
    -i, --interval INTEGER  设置延迟组的间隔时间（默认1200）
    --help                  Show this message and exit.
  
  
  # 示例
  ## 不自定义规则链接
  cs ss_link1 ss_link2 
  ## 自定义规则链接
  cs -r rule_link ss_link1 ss_link2
  ## 输出为 clash 配置文件
  cs -r rule_link ss_link -c
  ## 输出为 clash 配置文件，并且需要更改策略组名字
  cs ss_link1 ss_link2 -c -R
  ```

- 然后根据提示做完就可以了，能不能成功就随缘吧。:relieved: