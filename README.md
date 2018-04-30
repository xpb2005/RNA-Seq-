# miniconda-安装与使用(参考网上的资料，摘录下来方便自己用）
# 1. 首先在linux用户目录下新建一个文件夹
# mkdir /home/manager/software
# cd software
# 2. 下载miniconda,然后在对应目录下看到 miniconda/Miniconda3-latest-Linux-x86_64.sh文件
# wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
# 3. 安装
# bash Miniconda3-latest-Linux-x86_64.sh 
# 中间需要确认安装过程， 选yes就行
# source .bashrc  最开始没执行这个代码的时候不能用conda list，运行后就可以了。
# 安装完毕，可以输入 conda list 确认是否安装成功。
# 4. miniconda 使用
# 先添加频道（channels），然后才能使用conda安装生信的软件
# conda config --add channels r
# conda config --add channels defaults
# conda config --add channels conda-forge
# conda config --add channels bioconda
# Bioconda默认的chanel都在国外，下载软件非常缓慢，我们可以添加国内的chanel，以提高下载速度：
# conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
# conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
# conda config --set show_channel_urls yes
# conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge/
# conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/msys2/
# conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/bioconda/
# conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/menpo/
# 5. 使用conda安装fastqc
# conda install fastqc
# conda自动默认安装软件最新版本。询问要不要安装?这时候填 ”y“，程序继续自动安装,安装完后，在miniconda3/pkgs目录下会看到fastqc
# 可以使用which fastqc查看是否安装成功。
# 6. 安装其他软件使用类似方法
# conda install multiqc
# conda install trimmomatic
# conda install trinity
# 7. 其他命令
# 查询库中软件的版本： conda search 软件名
# 安装指定版本：conda install 软件名=版本号  （conda会卸载之前安装的版本，再重新安装）
# 更新版本 ：conda update 软件名
# 卸载软件  ：conda remove 软件名
# 激活软件 ： source activate 软件名  （把目录添加进环境变量）
# 钝化软件： source deactivate  （从环境变量里面 删去 ）
# 查看添加的频道 ：conda config --get channels
