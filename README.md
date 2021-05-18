# LinuxServer 实验室服务器操作手册

## 账号申请方法
联系当期服务器管理员
TODO

## 服务器介绍
这是王忠老师的实验室服务器，暂时不允许私自提供给实验室外的人员使用。TODO
服务器配置如下：

|                    |                               |
|:------------------:|:-----------------------------:|
|         CPU        | TODO 2*Silver 4210 2.2GHz 10C |
|         GPU        |    8 NVIDIA Tesla V100-32GB   |
|         RAM        |           4*32G DDR4          |
|        Cache       |     730i Raid 0,1,5 w/1GB     |
| Node-local storage |       480GB SSD + 8T HDD      |
|                    |                               |

- cuda版本为11.0，cudnn版本为8.0.5
- torch版本为1.8.1，tensorflow版本为2.4.0
- 可以使用jupyter工作

## 使用规则
TODO

## 校内ssh方法
目前ip是校内分配的ip，校外是无法访问的。不过你可以使用大工vpn尝试校外访问。TODO
现在的ip=210.30.97.81  
`ssh username@{ip}`  
`tap your password`

## 存储情况
目前给每人分配在固态硬盘上的工作空间是2GB，如果使用比较庞大的数据集，请放在机械硬盘上。硬盘结构如下图或者键入`lsblk`所示：  
![image](/pics/01.png)  
- `sda` 为480GB固态硬盘，`sdb`为8T机械硬盘。
- `/home`即所有用户的工作目录，在这个目录下每个用户会分配以你的名字命名的文件夹和2GB的工作空间。你可以把程序、小容量数据
集、配置文件存入你的工作空间里以更快的加载程序。
- `/local`为机械硬盘挂载的目录，目前所有用户均可以无限制使用，但请不要乱放你的文件。

## 安装你需要的python-package
`pip install [--user/-u] package-name`  
默认安装在你的工作目录/.local下。

## 如何传输文件？
- `scp` TODO
- 使用ftp工具FileZilla传输
- 使用shell工具传输

## 如何备份数据？

## 分区
用户与用户组操作见user_group目录

磁盘配额操作见quota目录

jupyter使用操作见jupyter目录

screen操作见screen目录

GPU操作见GPU目录

多核并行程序写法见parallel目录
