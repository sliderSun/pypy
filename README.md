用linux命令安装，如下：
sudo add-apt-repository ppa:pypy/ppa
sudo apt-get update
sudo apt-get install pypy pypy-dev

拷贝get-pip.py到linux
执行pypy get-pip.py

执行完之后，我们就可以使用pypy安装我们需要的第三方库了，比如我们想要安装xlwt：

pypy -m pip install xlwt

PyPy性能测试

写一个简单的小程序来测试PyPy的运行性能：

import datetime

time1 = datetime.datetime.now()
print (time1)for i in range(1000):    for j in range(1000):        for t in range(1000):
            pass
time2 = datetime.datetime.now()
print (time2)
print (time2-time1)
测试结果如下：


性能对比
可以发现PyPy的运行性能简直完爆使用默认的python环境的性能。
