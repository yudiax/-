第一天，在调用openai的api时，发现npm openai不能被识别
 发现nodejs需要本地安装包
在 F 盘的项目根目录 下执行：

bash
cd F:\你的项目路径
npm install openai  # 本地安装（会生成 node_modules）
优点：依赖会被安装到当前项目的 node_modules 中，确保项目独立性。

1.查看系统环境列表

conda info -e

2.创建虚拟环境（创建的环境路径\Anaconda3\envs）

conda create --name 环境名 （安装的包）

例如：conda create -n 环境名 python=3.8

3.激活环境

conda activate 环境名

4.查看环境里的包

conda list

5.关闭虚拟环境

conda deactivate

6.删除虚拟环境

conda remove -n 环境名 --all




2. 旧虚拟环境的 Kernel 未被清理
即使删除了 Miniconda，Jupyter 可能仍然保留旧内核的注册信息。

解决方法：手动移除旧 Kernel
查看当前 Jupyter Kernel 列表：

命令提示符
复制
jupyter kernelspec list
这会显示所有已注册的内核，例如：

复制
Available kernels:
  python3    C:\Users\YourUsername\AppData\Roaming\jupyter\kernels\python3
  old_env    C:\Users\YourUsername\AppData\Roaming\jupyter\kernels\old_env
删除不需要的 Kernel：

cmd
复制
jupyter kernelspec remove old_env
（替换 old_env 为你要删除的内核名称）

重新启动 Jupyter Notebook：

cmd
复制
jupyter notebook
现在应该只显示当前 Conda 环境中的内核。
