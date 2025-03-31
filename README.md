# googlehosts

### 本项目已放弃曾用域名googlehosts.org，请小心他人将域名用于制作钓鱼网站。

### Windows 修改 Hosts 方法

#### 1.打开 Hosts 文件

按 Win + R，输入 C:\Windows\System32\drivers\etc\hosts，回车。

选择 记事本 或 Notepad++ 作为编辑器。

#### 2.添加 Google Hosts 解析

在文件底部添加类似以下内容（具体 IP 地址需自行查找最新的）：

142.250.190.14 www.google.com
142.250.190.14 google.com
142.250.190.14 www.google.com.hk

#### 3.保存文件

由于 Hosts 受系统保护，需 管理员权限 保存。

可在 记事本 以“管理员身份运行”方式打开 Hosts 文件再编辑。

#### 4.清除 DNS 缓存

按 Win + R，输入 cmd，回车。

在命令提示符窗口中输入：

ipconfig /flushdns

这样就可以使修改的 Hosts 立即生效。

### Mac 修改 Hosts 方法

#### 1.打开终端

Command + 空格 搜索 Terminal 并打开。

编辑 Hosts 文件

#### 2.在终端输入：

sudo nano /etc/hosts

输入管理员密码后，进入 Nano 编辑器。

#### 3.添加 Google Hosts

在文件底部添加：

142.250.190.14 www.google.com
142.250.190.14 google.com

#### 4.保存修改

按 Control + X 退出，按 Y 保存，然后按 Enter 确认。

刷新 DNS 缓存

#### 5.在终端输入：

sudo killall -HUP mDNSResponder

### Linux 修改 Hosts 方法

#### 1.打开终端

#### 2.编辑 Hosts 文件

输入：
sudo nano /etc/hosts

#### 3.添加 Google Hosts

142.250.190.14 www.google.com
142.250.190.14 google.com

#### 4.保存并刷新 DNS

Control + X 退出，Y 保存。

刷新 DNS：

sudo systemctl restart nscd

### 注意事项
#### 1.获取最新 IP

Google 的 IP 可能会变化，可以使用 ping 命令获取：

ping www.google.com

或者使用第三方网站查询可用 Google IP。

#### 2.Hosts 方法可能失效

由于 Google 可能屏蔽 IP，Hosts 方式并不一定能稳定使用，建议使用 VPN 或代理工具。

#### 3.慎用公共 Hosts

从网上找的 Hosts 可能被篡改，建议自行测试有效 IP 以确保安全。




