# <font style="color:rgb(31, 35, 40);">1. Flag: </font>`<font style="color:rgb(31, 35, 40);background-color:rgba(129, 139, 152, 0.12);">NSSCTF {We1c0me\_t0\_WLLMCTF\_Th1s\_1s\_th3\_G1ft}</font>`
# <font style="color:rgb(31, 35, 40);">解题思路: F12 查看 HTML，Flag 隐藏在HTML代码中。</font>
**<font style="color:rgb(31, 35, 40);">2. 隐藏入口 (secret.php)</font>**

**<font style="color:rgb(31, 35, 40);">Flag: </font>**`**<font style="color:rgb(31, 35, 40);background-color:rgba(129, 139, 152, 0.12);">NSSCTF {0c659c79-c056-4932-870b-295b483de96d}</font>**`**<font style="color:rgb(31, 35, 40);"> [cite_start]</font>**

**<font style="color:rgb(31, 35, 40);">解题思路: 题目提供 </font>**`**<font style="color:rgb(31, 35, 40);background-color:rgba(129, 139, 152, 0.12);">secret.php</font>**`**<font style="color:rgb(31, 35, 40);">，通过输入框进入后台，获取账号密码登录后获取 Flag。</font>**

# **<font style="color:rgb(31, 35, 40);">Linux 学习笔记</font>**
## **<font style="color:rgb(31, 35, 40);">1. Linux 基础概念</font>**
### **<font style="color:rgb(31, 35, 40);">1.1 什么是 Linux？</font>**
+ **<font style="color:rgb(31, 35, 40);">Linux 是一个免费、开源、类 Unix 的操作系统内核。</font>**
+ **<font style="color:rgb(31, 35, 40);">基于 Linux 内核的操作系统称为发行版（如 Ubuntu、CentOS、Debian、Fedora）。</font>**

### **<font style="color:rgb(31, 35, 40);">1.2 核心特性</font>**
+ **<font style="color:rgb(31, 35, 40);">多用户、多任务</font>**
+ **<font style="color:rgb(31, 35, 40);">稳定、安全、高效</font>**
+ **<font style="color:rgb(31, 35, 40);">一切皆文件（硬件、目录、设备都表示为文件）</font>**

### **<font style="color:rgb(31, 35, 40);">1.3 常用发行版</font>**
| **<font style="color:rgb(31, 35, 40);">发行版</font>** | **<font style="color:rgb(31, 35, 40);">包管理工具</font>** | **<font style="color:rgb(31, 35, 40);">适用场景</font>** |
| --- | --- | --- |
| **<font style="color:rgb(31, 35, 40);">Ubuntu</font>** | **<font style="color:rgb(31, 35, 40);">apt</font>** | **<font style="color:rgb(31, 35, 40);">桌面、服务器、开发</font>** |
| **<font style="color:rgb(31, 35, 40);">CentOS / RHEL</font>** | **<font style="color:rgb(31, 35, 40);">yum / dnf</font>** | **<font style="color:rgb(31, 35, 40);">企业服务器</font>** |
| **<font style="color:rgb(31, 35, 40);">Debian</font>** | **<font style="color:rgb(31, 35, 40);">apt</font>** | **<font style="color:rgb(31, 35, 40);">稳定服务器</font>** |
| **<font style="color:rgb(31, 35, 40);">Fedora</font>** | **<font style="color:rgb(31, 35, 40);">dnf</font>** | **<font style="color:rgb(31, 35, 40);">最新技术体验</font>** |
| **<font style="color:rgb(31, 35, 40);">Arch Linux</font>** | **<font style="color:rgb(31, 35, 40);">pacman</font>** | **<font style="color:rgb(31, 35, 40);">高度定制化</font>** |


---

## **<font style="color:rgb(31, 35, 40);">2. Linux 文件系统</font>**
### **<font style="color:rgb(31, 35, 40);">2.1 目录结构（FHS 标准）</font>**
| **<font style="color:rgb(31, 35, 40);">目录</font>** | **<font style="color:rgb(31, 35, 40);">说明</font>** |
| --- | --- |
| **<font style="color:rgb(31, 35, 40);">/</font>** | **<font style="color:rgb(31, 35, 40);">根目录</font>** |
| **<font style="color:rgb(31, 35, 40);">/bin</font>** | **<font style="color:rgb(31, 35, 40);">基础系统命令（二进制文件）</font>** |
| **<font style="color:rgb(31, 35, 40);">/sbin</font>** | **<font style="color:rgb(31, 35, 40);">系统管理命令（需要 root 权限）</font>** |
| **<font style="color:rgb(31, 35, 40);">/etc</font>** | **<font style="color:rgb(31, 35, 40);">配置文件</font>** |
| **<font style="color:rgb(31, 35, 40);">/home</font>** | **<font style="color:rgb(31, 35, 40);">普通用户的家目录</font>** |
| **<font style="color:rgb(31, 35, 40);">/root</font>** | **<font style="color:rgb(31, 35, 40);">root 用户的家目录</font>** |
| **<font style="color:rgb(31, 35, 40);">/var</font>** | **<font style="color:rgb(31, 35, 40);">可变数据（日志、缓存、邮件）</font>** |
| **<font style="color:rgb(31, 35, 40);">/tmp</font>** | **<font style="color:rgb(31, 35, 40);">临时文件（重启后可能清空）</font>** |
| **<font style="color:rgb(31, 35, 40);">/usr</font>** | **<font style="color:rgb(31, 35, 40);">用户程序和数据（类似 Windows 的 Program Files）</font>** |
| **<font style="color:rgb(31, 35, 40);">/proc</font>** | **<font style="color:rgb(31, 35, 40);">虚拟文件系统，存储进程和内核信息</font>** |


### **<font style="color:rgb(31, 35, 40);">2.2 路径表示</font>**
+ **绝对路径****<font style="color:rgb(31, 35, 40);">：从根 </font>**`**<font style="color:rgb(31, 35, 40);">/</font>**`**<font style="color:rgb(31, 35, 40);"> 开始，如 </font>**`**<font style="color:rgb(31, 35, 40);">/home/user/file.txt</font>**`
+ **相对路径****<font style="color:rgb(31, 35, 40);">：相对于当前目录，如 </font>**`**<font style="color:rgb(31, 35, 40);">./file.txt</font>**`**<font style="color:rgb(31, 35, 40);">、</font>**`**<font style="color:rgb(31, 35, 40);">../dir/</font>**`

---

## **<font style="color:rgb(31, 35, 40);">3. 基础命令</font>**
### **<font style="color:rgb(31, 35, 40);">3.1 文件和目录操作</font>**
| **<font style="color:rgb(31, 35, 40);">命令</font>** | **<font style="color:rgb(31, 35, 40);">作用</font>** | **<font style="color:rgb(31, 35, 40);">示例</font>** |
| --- | --- | --- |
| `**<font style="color:rgb(31, 35, 40);">ls</font>**` | **<font style="color:rgb(31, 35, 40);">列出目录内容</font>** | `**<font style="color:rgb(31, 35, 40);">ls -la</font>**`**<font style="color:rgb(31, 35, 40);">（显示所有文件详情）</font>** |
| `**<font style="color:rgb(31, 35, 40);">cd</font>**` | **<font style="color:rgb(31, 35, 40);">切换目录</font>** | `**<font style="color:rgb(31, 35, 40);">cd /etc</font>**` |
| `**<font style="color:rgb(31, 35, 40);">pwd</font>**` | **<font style="color:rgb(31, 35, 40);">显示当前路径</font>** | `**<font style="color:rgb(31, 35, 40);">pwd</font>**` |
| `**<font style="color:rgb(31, 35, 40);">mkdir</font>**` | **<font style="color:rgb(31, 35, 40);">创建目录</font>** | `**<font style="color:rgb(31, 35, 40);">mkdir -p a/b/c</font>**`**<font style="color:rgb(31, 35, 40);">（递归创建）</font>** |
| `**<font style="color:rgb(31, 35, 40);">rmdir</font>**` | **<font style="color:rgb(31, 35, 40);">删除空目录</font>** | `**<font style="color:rgb(31, 35, 40);">rmdir empty_dir</font>**` |
| `**<font style="color:rgb(31, 35, 40);">rm</font>**` | **<font style="color:rgb(31, 35, 40);">删除文件或目录</font>** | `**<font style="color:rgb(31, 35, 40);">rm -rf dir/</font>**`**<font style="color:rgb(31, 35, 40);">（强制递归删除）</font>** |
| `**<font style="color:rgb(31, 35, 40);">cp</font>**` | **<font style="color:rgb(31, 35, 40);">复制文件或目录</font>** | `**<font style="color:rgb(31, 35, 40);">cp -r src/ dst/</font>**` |
| `**<font style="color:rgb(31, 35, 40);">mv</font>**` | **<font style="color:rgb(31, 35, 40);">移动/重命名</font>** | `**<font style="color:rgb(31, 35, 40);">mv old.txt new.txt</font>**` |
| `**<font style="color:rgb(31, 35, 40);">touch</font>**` | **<font style="color:rgb(31, 35, 40);">创建空文件或更新时间戳</font>** | `**<font style="color:rgb(31, 35, 40);">touch file.txt</font>**` |
| `**<font style="color:rgb(31, 35, 40);">file</font>**` | **<font style="color:rgb(31, 35, 40);">查看文件类型</font>** | `**<font style="color:rgb(31, 35, 40);">file script.sh</font>**` |


### **<font style="color:rgb(31, 35, 40);">3.2 查看文件内容</font>**
| **<font style="color:rgb(31, 35, 40);">命令</font>** | **<font style="color:rgb(31, 35, 40);">作用</font>** | **<font style="color:rgb(31, 35, 40);">示例</font>** |
| --- | --- | --- |
| `**<font style="color:rgb(31, 35, 40);">cat</font>**` | **<font style="color:rgb(31, 35, 40);">显示全部内容</font>** | `**<font style="color:rgb(31, 35, 40);">cat file.txt</font>**` |
| `**<font style="color:rgb(31, 35, 40);">less</font>**` | **<font style="color:rgb(31, 35, 40);">分页浏览（空格翻页，q 退出）</font>** | `**<font style="color:rgb(31, 35, 40);">less large.log</font>**` |
| `**<font style="color:rgb(31, 35, 40);">head</font>**` | **<font style="color:rgb(31, 35, 40);">显示前10行</font>** | `**<font style="color:rgb(31, 35, 40);">head -n 20 file</font>**` |
| `**<font style="color:rgb(31, 35, 40);">tail</font>**` | **<font style="color:rgb(31, 35, 40);">显示后10行</font>** | `**<font style="color:rgb(31, 35, 40);">tail -f log</font>**`**<font style="color:rgb(31, 35, 40);">（实时跟踪）</font>** |
| `**<font style="color:rgb(31, 35, 40);">grep</font>**` | **<font style="color:rgb(31, 35, 40);">搜索文本</font>** | `**<font style="color:rgb(31, 35, 40);">grep "error" log</font>**` |


### **<font style="color:rgb(31, 35, 40);">3.3 权限管理</font>**
+ **权限表示****<font style="color:rgb(31, 35, 40);">：</font>**`**<font style="color:rgb(31, 35, 40);">rwxr-xr--</font>**`**<font style="color:rgb(31, 35, 40);"> 分为三组（所有者、组、其他）</font>**

| **<font style="color:rgb(31, 35, 40);">命令</font>** | **<font style="color:rgb(31, 35, 40);">作用</font>** | **<font style="color:rgb(31, 35, 40);">示例</font>** |
| --- | --- | --- |
| `**<font style="color:rgb(31, 35, 40);">chmod</font>**` | **<font style="color:rgb(31, 35, 40);">修改权限（符号或数字）</font>** | `**<font style="color:rgb(31, 35, 40);">chmod 755 script.sh</font>**` |
| `**<font style="color:rgb(31, 35, 40);">chown</font>**` | **<font style="color:rgb(31, 35, 40);">修改所有者:组</font>** | `**<font style="color:rgb(31, 35, 40);">chown user:group file</font>**` |
| `**<font style="color:rgb(31, 35, 40);">chgrp</font>**` | **<font style="color:rgb(31, 35, 40);">修改所属组</font>** | `**<font style="color:rgb(31, 35, 40);">chgrp staff file</font>**` |


    - `**<font style="color:rgb(31, 35, 40);">r</font>**`**<font style="color:rgb(31, 35, 40);"> = 读（4）</font>**
    - `**<font style="color:rgb(31, 35, 40);">w</font>**`**<font style="color:rgb(31, 35, 40);"> = 写（2）</font>**
    - `**<font style="color:rgb(31, 35, 40);">x</font>**`**<font style="color:rgb(31, 35, 40);"> = 执行（1）</font>**

### **<font style="color:rgb(31, 35, 40);">3.4 帮助文档</font>**
| **<font style="color:rgb(31, 35, 40);">命令</font>** | **<font style="color:rgb(31, 35, 40);">作用</font>** | **<font style="color:rgb(31, 35, 40);">示例</font>** |
| --- | --- | --- |
| `**<font style="color:rgb(31, 35, 40);">man</font>**` | **<font style="color:rgb(31, 35, 40);">查看命令手册</font>** | `**<font style="color:rgb(31, 35, 40);">man ls</font>**` |
| `**<font style="color:rgb(31, 35, 40);">info</font>**` | **<font style="color:rgb(31, 35, 40);">更详细的文档</font>** | `**<font style="color:rgb(31, 35, 40);">info coreutils</font>**` |
| `**<font style="color:rgb(31, 35, 40);">--help</font>**` | **<font style="color:rgb(31, 35, 40);">简要帮助</font>** | `**<font style="color:rgb(31, 35, 40);">ls --help</font>**` |


---

## **<font style="color:rgb(31, 35, 40);">4. 用户与组管理</font>**
### **<font style="color:rgb(31, 35, 40);">4.1 用户管理</font>**
| **<font style="color:rgb(31, 35, 40);">命令</font>** | **<font style="color:rgb(31, 35, 40);">作用</font>** | **<font style="color:rgb(31, 35, 40);">示例</font>** |
| --- | --- | --- |
| `**<font style="color:rgb(31, 35, 40);">useradd</font>**` | **<font style="color:rgb(31, 35, 40);">创建用户</font>** | `**<font style="color:rgb(31, 35, 40);">useradd -m -s /bin/bash alice</font>**` |
| `**<font style="color:rgb(31, 35, 40);">passwd</font>**` | **<font style="color:rgb(31, 35, 40);">设置/修改密码</font>** | `**<font style="color:rgb(31, 35, 40);">passwd alice</font>**` |
| `**<font style="color:rgb(31, 35, 40);">usermod</font>**` | **<font style="color:rgb(31, 35, 40);">修改用户属性</font>** | `**<font style="color:rgb(31, 35, 40);">usermod -aG sudo alice</font>**` |
| `**<font style="color:rgb(31, 35, 40);">userdel</font>**` | **<font style="color:rgb(31, 35, 40);">删除用户</font>** | `**<font style="color:rgb(31, 35, 40);">userdel -r alice</font>**`**<font style="color:rgb(31, 35, 40);">（同时删除家目录）</font>** |
| `**<font style="color:rgb(31, 35, 40);">whoami</font>**` | **<font style="color:rgb(31, 35, 40);">显示当前用户名</font>** | `**<font style="color:rgb(31, 35, 40);">whoami</font>**` |
| `**<font style="color:rgb(31, 35, 40);">id</font>**` | **<font style="color:rgb(31, 35, 40);">显示用户ID和组信息</font>** | `**<font style="color:rgb(31, 35, 40);">id alice</font>**` |


### **<font style="color:rgb(31, 35, 40);">4.2 组管理</font>**
| **<font style="color:rgb(31, 35, 40);">命令</font>** | **<font style="color:rgb(31, 35, 40);">作用</font>** | **<font style="color:rgb(31, 35, 40);">示例</font>** |
| --- | --- | --- |
| `**<font style="color:rgb(31, 35, 40);">groupadd</font>**` | **<font style="color:rgb(31, 35, 40);">创建组</font>** | `**<font style="color:rgb(31, 35, 40);">groupadd dev</font>**` |
| `**<font style="color:rgb(31, 35, 40);">groupdel</font>**` | **<font style="color:rgb(31, 35, 40);">删除组</font>** | `**<font style="color:rgb(31, 35, 40);">groupdel dev</font>**` |
| `**<font style="color:rgb(31, 35, 40);">groups</font>**` | **<font style="color:rgb(31, 35, 40);">显示用户所属组</font>** | `**<font style="color:rgb(31, 35, 40);">groups alice</font>**` |


### **<font style="color:rgb(31, 35, 40);">4.3 切换用户</font>**
| **<font style="color:rgb(31, 35, 40);">命令</font>** | **<font style="color:rgb(31, 35, 40);">作用</font>** | **<font style="color:rgb(31, 35, 40);">示例</font>** |
| --- | --- | --- |
| `**<font style="color:rgb(31, 35, 40);">su</font>**` | **<font style="color:rgb(31, 35, 40);">切换用户（需目标用户密码）</font>** | `**<font style="color:rgb(31, 35, 40);">su - alice</font>**` |
| `**<font style="color:rgb(31, 35, 40);">sudo</font>**` | **<font style="color:rgb(31, 35, 40);">以 root 权限执行命令</font>** | `**<font style="color:rgb(31, 35, 40);">sudo apt update</font>**` |


---

## **<font style="color:rgb(31, 35, 40);">5. 进程管理</font>**
| **<font style="color:rgb(31, 35, 40);">命令</font>** | **<font style="color:rgb(31, 35, 40);">作用</font>** | **<font style="color:rgb(31, 35, 40);">示例</font>** |
| --- | --- | --- |
| `**<font style="color:rgb(31, 35, 40);">ps</font>**` | **<font style="color:rgb(31, 35, 40);">查看进程</font>** | `**<font style="color:rgb(31, 35, 40);">ps aux</font>**`**<font style="color:rgb(31, 35, 40);">（所有进程详细）</font>** |
| `**<font style="color:rgb(31, 35, 40);">top</font>**` | **<font style="color:rgb(31, 35, 40);">动态进程监控（类似任务管理器）</font>** | `**<font style="color:rgb(31, 35, 40);">top</font>**` |
| `**<font style="color:rgb(31, 35, 40);">htop</font>**` | **<font style="color:rgb(31, 35, 40);">增强版 top（需安装）</font>** | `**<font style="color:rgb(31, 35, 40);">htop</font>**` |
| `**<font style="color:rgb(31, 35, 40);">kill</font>**` | **<font style="color:rgb(31, 35, 40);">终止进程</font>** | `**<font style="color:rgb(31, 35, 40);">kill -9 PID</font>**`**<font style="color:rgb(31, 35, 40);">（强制终止）</font>** |
| `**<font style="color:rgb(31, 35, 40);">pkill</font>**` | **<font style="color:rgb(31, 35, 40);">按名称终止</font>** | `**<font style="color:rgb(31, 35, 40);">pkill firefox</font>**` |
| `**<font style="color:rgb(31, 35, 40);">jobs</font>**` | **<font style="color:rgb(31, 35, 40);">查看后台任务</font>** | `**<font style="color:rgb(31, 35, 40);">jobs</font>**` |
| `**<font style="color:rgb(31, 35, 40);">bg</font>**`**<font style="color:rgb(31, 35, 40);"> / </font>**`**<font style="color:rgb(31, 35, 40);">fg</font>**` | **<font style="color:rgb(31, 35, 40);">任务前后台切换</font>** | `**<font style="color:rgb(31, 35, 40);">bg %1</font>**` |
| `**<font style="color:rgb(31, 35, 40);">nohup</font>**` | **<font style="color:rgb(31, 35, 40);">忽略挂断信号运行</font>** | `**<font style="color:rgb(31, 35, 40);">nohup ./server &</font>**` |


---

## **<font style="color:rgb(31, 35, 40);">6. 软件包管理</font>**
### **<font style="color:rgb(31, 35, 40);">6.1 Debian/Ubuntu (apt)</font>**
| **<font style="color:rgb(31, 35, 40);">命令</font>** | **<font style="color:rgb(31, 35, 40);">作用</font>** |
| --- | --- |
| `**<font style="color:rgb(31, 35, 40);">sudo apt update</font>**` | **<font style="color:rgb(31, 35, 40);">更新软件源列表</font>** |
| `**<font style="color:rgb(31, 35, 40);">sudo apt upgrade</font>**` | **<font style="color:rgb(31, 35, 40);">升级所有可升级的软件包</font>** |
| `**<font style="color:rgb(31, 35, 40);">sudo apt install <pkg></font>**` | **<font style="color:rgb(31, 35, 40);">安装软件包</font>** |
| `**<font style="color:rgb(31, 35, 40);">sudo apt remove <pkg></font>**` | **<font style="color:rgb(31, 35, 40);">删除软件包（保留配置）</font>** |
| `**<font style="color:rgb(31, 35, 40);">sudo apt purge <pkg></font>**` | **<font style="color:rgb(31, 35, 40);">彻底删除（含配置）</font>** |
| `**<font style="color:rgb(31, 35, 40);">apt search <keyword></font>**` | **<font style="color:rgb(31, 35, 40);">搜索软件包</font>** |
| `**<font style="color:rgb(31, 35, 40);">apt show <pkg></font>**` | **<font style="color:rgb(31, 35, 40);">显示软件包详情</font>** |


### **<font style="color:rgb(31, 35, 40);">6.2 CentOS/RHEL (yum/dnf)</font>**
| **<font style="color:rgb(31, 35, 40);">命令</font>** | **<font style="color:rgb(31, 35, 40);">作用</font>** |
| --- | --- |
| `**<font style="color:rgb(31, 35, 40);">sudo yum install <pkg></font>**` | **<font style="color:rgb(31, 35, 40);">安装</font>** |
| `**<font style="color:rgb(31, 35, 40);">sudo yum remove <pkg></font>**` | **<font style="color:rgb(31, 35, 40);">删除</font>** |
| `**<font style="color:rgb(31, 35, 40);">sudo yum search <keyword></font>**` | **<font style="color:rgb(31, 35, 40);">搜索</font>** |
| `**<font style="color:rgb(31, 35, 40);">sudo yum update</font>**` | **<font style="color:rgb(31, 35, 40);">更新所有包</font>** |


### **<font style="color:rgb(31, 35, 40);">6.3 编译源码安装</font>**
```bash
./configure --prefix=/usr/local/app
make
sudo make install
```

---

## **<font style="color:rgb(31, 35, 40);">7. 网络配置与管理</font>**
| **<font style="color:rgb(31, 35, 40);">命令</font>** | **<font style="color:rgb(31, 35, 40);">作用</font>** | **<font style="color:rgb(31, 35, 40);">示例</font>** |
| --- | --- | --- |
| `**<font style="color:rgb(31, 35, 40);">ip addr</font>**`**<font style="color:rgb(31, 35, 40);"> / </font>**`**<font style="color:rgb(31, 35, 40);">ifconfig</font>**` | **<font style="color:rgb(31, 35, 40);">查看IP地址（需安装net-tools）</font>** | `**<font style="color:rgb(31, 35, 40);">ip a</font>**` |
| `**<font style="color:rgb(31, 35, 40);">ping</font>**` | **<font style="color:rgb(31, 35, 40);">测试连通性</font>** | `**<font style="color:rgb(31, 35, 40);">ping google.com</font>**` |
| `**<font style="color:rgb(31, 35, 40);">curl</font>**` | **<font style="color:rgb(31, 35, 40);">发送HTTP请求/下载</font>** | `**<font style="color:rgb(31, 35, 40);">curl -O http://example.com/file</font>**` |
| `**<font style="color:rgb(31, 35, 40);">wget</font>**` | **<font style="color:rgb(31, 35, 40);">下载文件</font>** | `**<font style="color:rgb(31, 35, 40);">wget http://example.com/file</font>**` |
| `**<font style="color:rgb(31, 35, 40);">netstat</font>**`**<font style="color:rgb(31, 35, 40);"> / </font>**`**<font style="color:rgb(31, 35, 40);">ss</font>**` | **<font style="color:rgb(31, 35, 40);">查看网络连接和端口</font>** | `**<font style="color:rgb(31, 35, 40);">ss -tuln</font>**`**<font style="color:rgb(31, 35, 40);">（监听端口）</font>** |
| `**<font style="color:rgb(31, 35, 40);">ssh</font>**` | **<font style="color:rgb(31, 35, 40);">远程登录</font>** | `**<font style="color:rgb(31, 35, 40);">ssh user@host</font>**` |
| `**<font style="color:rgb(31, 35, 40);">scp</font>**` | **<font style="color:rgb(31, 35, 40);">安全复制（基于SSH）</font>** | `**<font style="color:rgb(31, 35, 40);">scp file user@host:/path/</font>**` |
| `**<font style="color:rgb(31, 35, 40);">rsync</font>**` | **<font style="color:rgb(31, 35, 40);">增量同步</font>** | `**<font style="color:rgb(31, 35, 40);">rsync -av src/ dst/</font>**` |


### **<font style="color:rgb(31, 35, 40);">7.1 防火墙（以 ufw 为例）</font>**
```bash
sudo ufw enable                # 启用防火墙
sudo ufw allow 22/tcp          # 允许 SSH
sudo ufw allow 80/tcp          # 允许 HTTP
sudo ufw status verbose        # 查看状态
```

---

## **<font style="color:rgb(31, 35, 40);">8. 文本编辑器</font>**
+ **vim****<font style="color:rgb(31, 35, 40);">：终端下强大编辑器，需学习模式切换（普通模式、插入模式、命令模式）</font>**
    - **<font style="color:rgb(31, 35, 40);">基本操作：</font>**`**<font style="color:rgb(31, 35, 40);">i</font>**`**<font style="color:rgb(31, 35, 40);"> 进入插入，</font>**`**<font style="color:rgb(31, 35, 40);">Esc</font>**`**<font style="color:rgb(31, 35, 40);"> 退出插入，</font>**`**<font style="color:rgb(31, 35, 40);">:wq</font>**`**<font style="color:rgb(31, 35, 40);"> 保存退出，</font>**`**<font style="color:rgb(31, 35, 40);">:q!</font>**`**<font style="color:rgb(31, 35, 40);"> 不保存退出</font>**
+ **nano****<font style="color:rgb(31, 35, 40);">：简单易用，适合新手，屏幕底部有快捷键提示</font>**
+ **gedit****<font style="color:rgb(31, 35, 40);">：图形化编辑器</font>**

---

## **<font style="color:rgb(31, 35, 40);">9. 压缩与归档</font>**
| **<font style="color:rgb(31, 35, 40);">命令</font>** | **<font style="color:rgb(31, 35, 40);">作用</font>** | **<font style="color:rgb(31, 35, 40);">示例</font>** |
| --- | --- | --- |
| `**<font style="color:rgb(31, 35, 40);">tar</font>**` | **<font style="color:rgb(31, 35, 40);">打包/解包（常与压缩结合）</font>** | `**<font style="color:rgb(31, 35, 40);">tar -czvf archive.tar.gz dir/</font>**`**<font style="color:rgb(31, 35, 40);">（打包压缩）</font>****<font style="color:rgb(31, 35, 40);">   </font>**`**<font style="color:rgb(31, 35, 40);">tar -xzvf archive.tar.gz</font>**`**<font style="color:rgb(31, 35, 40);">（解压）</font>** |
| `**<font style="color:rgb(31, 35, 40);">zip</font>**`**<font style="color:rgb(31, 35, 40);"> / </font>**`**<font style="color:rgb(31, 35, 40);">unzip</font>**` | **<font style="color:rgb(31, 35, 40);">zip格式压缩/解压</font>** | `**<font style="color:rgb(31, 35, 40);">zip -r archive.zip dir/</font>**`**<font style="color:rgb(31, 35, 40);">   </font>**`**<font style="color:rgb(31, 35, 40);">unzip archive.zip</font>**` |
| `**<font style="color:rgb(31, 35, 40);">gzip</font>**` | **<font style="color:rgb(31, 35, 40);">单文件压缩（.gz）</font>** | `**<font style="color:rgb(31, 35, 40);">gzip file.txt</font>**` |


---

## **<font style="color:rgb(31, 35, 40);">10. 系统信息与监控</font>**
| **<font style="color:rgb(31, 35, 40);">命令</font>** | **<font style="color:rgb(31, 35, 40);">作用</font>** |
| --- | --- |
| `**<font style="color:rgb(31, 35, 40);">uname -a</font>**` | **<font style="color:rgb(31, 35, 40);">显示内核版本、主机名等</font>** |
| `**<font style="color:rgb(31, 35, 40);">df -h</font>**` | **<font style="color:rgb(31, 35, 40);">查看磁盘分区使用情况</font>** |
| `**<font style="color:rgb(31, 35, 40);">du -sh</font>**` | **<font style="color:rgb(31, 35, 40);">查看目录或文件大小</font>** |
| `**<font style="color:rgb(31, 35, 40);">free -h</font>**` | **<font style="color:rgb(31, 35, 40);">查看内存和 swap 使用情况</font>** |
| `**<font style="color:rgb(31, 35, 40);">uptime</font>**` | **<font style="color:rgb(31, 35, 40);">系统运行时间及负载</font>** |
| `**<font style="color:rgb(31, 35, 40);">dmesg</font>**` | **<font style="color:rgb(31, 35, 40);">查看内核日志（硬件检测等）</font>** |


---

## **<font style="color:rgb(31, 35, 40);">11. 常用技巧与快捷键</font>**
### **<font style="color:rgb(31, 35, 40);">11.1 命令行快捷键</font>**
| **<font style="color:rgb(31, 35, 40);">快捷键</font>** | **<font style="color:rgb(31, 35, 40);">作用</font>** |
| --- | --- |
| `**<font style="color:rgb(31, 35, 40);">Tab</font>**` | **<font style="color:rgb(31, 35, 40);">自动补全命令/路径</font>** |
| `**<font style="color:rgb(31, 35, 40);">Ctrl + C</font>**` | **<font style="color:rgb(31, 35, 40);">终止当前进程</font>** |
| `**<font style="color:rgb(31, 35, 40);">Ctrl + Z</font>**` | **<font style="color:rgb(31, 35, 40);">暂停进程（放入后台）</font>** |
| `**<font style="color:rgb(31, 35, 40);">Ctrl + D</font>**` | **<font style="color:rgb(31, 35, 40);">退出当前终端（发送 EOF）</font>** |
| `**<font style="color:rgb(31, 35, 40);">Ctrl + L</font>**` | **<font style="color:rgb(31, 35, 40);">清屏（类似 </font>**`**<font style="color:rgb(31, 35, 40);">clear</font>**`**<font style="color:rgb(31, 35, 40);">）</font>** |
| `**<font style="color:rgb(31, 35, 40);">Ctrl + A</font>**` | **<font style="color:rgb(31, 35, 40);">光标移至行首</font>** |
| `**<font style="color:rgb(31, 35, 40);">Ctrl + E</font>**` | **<font style="color:rgb(31, 35, 40);">光标移至行尾</font>** |
| `**<font style="color:rgb(31, 35, 40);">↑</font>**`**<font style="color:rgb(31, 35, 40);"> / </font>**`**<font style="color:rgb(31, 35, 40);">↓</font>**` | **<font style="color:rgb(31, 35, 40);">浏览命令历史</font>** |
| `**<font style="color:rgb(31, 35, 40);">!!</font>**` | **<font style="color:rgb(31, 35, 40);">重复上一条命令</font>** |
| `**<font style="color:rgb(31, 35, 40);">!n</font>**` | **<font style="color:rgb(31, 35, 40);">执行历史中第 n 条命令</font>** |


### **<font style="color:rgb(31, 35, 40);">11.2 重定向与管道</font>**
+ **重定向****<font style="color:rgb(31, 35, 40);">：</font>**
    - `**<font style="color:rgb(31, 35, 40);">></font>**`**<font style="color:rgb(31, 35, 40);">  覆盖输出到文件</font>**
    - `**<font style="color:rgb(31, 35, 40);">>></font>**`**<font style="color:rgb(31, 35, 40);"> 追加输出到文件</font>**
    - `**<font style="color:rgb(31, 35, 40);">2></font>**`**<font style="color:rgb(31, 35, 40);"> 重定向错误输出</font>**
    - `**<font style="color:rgb(31, 35, 40);">&></font>**`**<font style="color:rgb(31, 35, 40);"> 重定向所有输出</font>**
+ **管道 **`**<font style="color:rgb(31, 35, 40);">|</font>**`**<font style="color:rgb(31, 35, 40);">：将前一个命令的输出作为后一个命令的输入</font>**

```bash
ls -la | grep ".txt" | wc -l
```

---

## **<font style="color:rgb(31, 35, 40);">12. 简单 Shell 脚本</font>**
### **<font style="color:rgb(31, 35, 40);">12.1 基本结构</font>**
```bash
#!/bin/bash
# 这是一个注释
echo "Hello, World!"
```

### **<font style="color:rgb(31, 35, 40);">12.2 变量</font>**
```bash
name="Alice"
echo "My name is $name"
```

### **<font style="color:rgb(31, 35, 40);">12.3 条件判断</font>**
```bash
if [ -f "$file" ]; then
    echo "$file exists"
else
    echo "Not found"
fi
```

### **<font style="color:rgb(31, 35, 40);">12.4 循环</font>**
```bash
for i in {1..5}; do
    echo "Number $i"
done
```

### **<font style="color:rgb(31, 35, 40);">12.5 执行脚本</font>**
```bash
chmod +x script.sh
./script.sh
# 或
bash script.sh
```

---

## **<font style="color:rgb(31, 35, 40);">13. 常见问题排查思路</font>**
| **<font style="color:rgb(31, 35, 40);">问题类型</font>** | **<font style="color:rgb(31, 35, 40);">常用命令/方法</font>** |
| --- | --- |
| **<font style="color:rgb(31, 35, 40);">磁盘满</font>** | `**<font style="color:rgb(31, 35, 40);">df -h</font>**`**<font style="color:rgb(31, 35, 40);"> 查看使用率；</font>**`**<font style="color:rgb(31, 35, 40);">du -sh /*</font>**`**<font style="color:rgb(31, 35, 40);"> 找大文件</font>** |
| **<font style="color:rgb(31, 35, 40);">CPU 高负载</font>** | `**<font style="color:rgb(31, 35, 40);">top</font>**`**<font style="color:rgb(31, 35, 40);"> / </font>**`**<font style="color:rgb(31, 35, 40);">htop</font>**`**<font style="color:rgb(31, 35, 40);"> 看进程；</font>**`**<font style="color:rgb(31, 35, 40);">ps aux --sort=-%cpu</font>**` |
| **<font style="color:rgb(31, 35, 40);">内存不足</font>** | `**<font style="color:rgb(31, 35, 40);">free -h</font>**`**<font style="color:rgb(31, 35, 40);">；</font>**`**<font style="color:rgb(31, 35, 40);">ps aux --sort=-%mem</font>**` |
| **<font style="color:rgb(31, 35, 40);">端口被占用</font>** | `**<font style="color:rgb(31, 35, 40);">ss -tuln</font>**`**<font style="color:rgb(31, 35, 40);"> 或 </font>**`**<font style="color:rgb(31, 35, 40);">netstat -tuln</font>**`**<font style="color:rgb(31, 35, 40);">；</font>**`**<font style="color:rgb(31, 35, 40);">lsof -i:端口号</font>**` |
| **<font style="color:rgb(31, 35, 40);">无法上网</font>** | `**<font style="color:rgb(31, 35, 40);">ping 8.8.8.8</font>**`**<font style="color:rgb(31, 35, 40);">；检查 DNS </font>**`**<font style="color:rgb(31, 35, 40);">cat /etc/resolv.conf</font>**`**<font style="color:rgb(31, 35, 40);">；</font>**`**<font style="color:rgb(31, 35, 40);">ip a</font>**`**<font style="color:rgb(31, 35, 40);"> 看IP配置</font>** |
| **<font style="color:rgb(31, 35, 40);">权限被拒绝</font>** | **<font style="color:rgb(31, 35, 40);">检查文件权限 </font>**`**<font style="color:rgb(31, 35, 40);">ls -l</font>**`**<font style="color:rgb(31, 35, 40);">；使用 </font>**`**<font style="color:rgb(31, 35, 40);">sudo</font>**`**<font style="color:rgb(31, 35, 40);">；查看用户组 </font>**`**<font style="color:rgb(31, 35, 40);">id</font>**` |


安装  
1.Burpsuit：参考博客 burpsuit下载

2.hackbar：参考博客 hackbar插件安装教程  
3.dirsearch：参考 dirsearch的安装(非常详细)和使用  
4.linux：Ubuntu  
5.AI：DeepSeek

