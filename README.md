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
