### 代码环境：
    1.代码是采用的是TensorFlow深度学习框架，版本Tensorflow 1.12.0
    2.依赖包有：
      （1）CUDA 9.0.176、CUDNN 7.4.2
                首先把CUDA安装包下载到~/Downloads文件夹下，打开终端，输入命令：
                sudo dpkg -i cuda-repo-ubuntu1604-9-0-local_9.0.176-1_amd64.deb
                sudo apt-key add /var/cuda-repo-9-0-local/7fa2af80.pub
                sudo apt-get update
                sudo apt-get install cuda
                CUDA安装完成后，还需添加环境变量，打开终端，输入命令：
                export PATH=/usr/local/cuda-9.0/bin${PATH:+:${PATH}}
                export LD_LIBRARY_PATH=/usr/local/cuda-9.0/lib64${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}} #64位系统
                然后nvidia官网下载对应CUDA的cuDNN7.4.2版本，同样的下载目录，打开终端，输入命令：
                sudo dpkg -i libcudnn7_7.4.2.24-1+cuda9.0_amd64.deb
      （2）python package有：os、math、time、glob、numpy、random、matplotlib
                终端安装命令：
                pip install os
                pip install math
                pip install time
                pip install glob
                pip install numpy
                pip install random
                pip install matplotlib
    3.CUDA、CUDNN版本： CUDA 9.0.176、CUDNN 7.4.2   

### 训练和推理的执行：
    1.运行generate_data.py生成data数据集
    2.train.py是训练程序文件，生成模型
    3.test.py是推理（测试）文件，输入测试集低分辨率视频，输出高分辨预测视频
    相应的sh命令: 
    python generate_data.py
    python train.py
    python test.py

​    
