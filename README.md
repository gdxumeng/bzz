## 注意！官方已更新至0.6.0版本，而本脚本用的仍是0.5.3。

## 前言  
这是一个自用脚本，因此不能满足所有人的需求。有需要的朋友欢迎fork修改。


## 环境
Ubuntu20.04
未安装Bee或已将其彻底删除，/var、/etc目录下无残留。


## 功能
step1.sh:  
配置节点。  
step2.sh:  
开启节点，设置自动兑付，下载钱包文件。钱包文件不能直接导入小狐狸，请自行转换。  
转换可参考：https://github.com/ethersphere/exportSwarmKey  
step3.sh:  
下载合约地址、钱包地址的txt文件。


## 用法
#### 配置节点
wget https://raw.githubusercontent.com/pumpkin4gb/bzz/main/step1.sh && chmod 777 step1.sh && ./step1.sh  
之后每想添加一个节点就运行一次./step1.sh，直至满意数量。  
运行./step2.sh开启节点。  
#### 手动提票  
对节点1提票：  
cashout1.sh cashout-all
其他节点同理。正常会自动提，无须手动。  
#### 获取地址  
./step3.sh  
如提示无step3.sh文件，手动下载step3.sh上传即可。  
若有获取的节点地址为空，大概率是服务器配置不够，小概率是endpoint爆满。  
近期测试网拥堵，新建的节点亦有可能出现此情况。等待数据同步后再获取即可。


## 其他问题  
~~如果运行cashout1.sh时报1634+错误，运行fix_port.sh修复即可~~  
~~如果发现没有自动提票，运行fix_cash.sh修复即可~~  
新版本已修复。
