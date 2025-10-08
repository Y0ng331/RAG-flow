# RAG-flow
首先下载安装ollama，下载所需要的模型；
之后下载docker，windows注意下载AMD版本的；
之后去github-RAG官网拉取RAG包，按照readme修改配置文件（env）；
之后按照B站用户提示修改：1、修改docker软件右上角设置中的资源项，将磁盘镜像位置调整至ragflow-main文件夹下的docker文件夹内
2、修改docker软件右上角设置中的Docker引擎项，可以新增加代码
"registry-mirrors": 【
"https://docker.1ms.run"
】
3、下载完成之后ragflow-main文件夹差不多有三十个G，因此要提前留好空间，下载可能持续几十个小时，如果中间下载停止，可以再次输入指令运行，即可再次下载。[链接](https://www.bilibili.com/video/BV1WiP2ezE5a/?spm_id_from=333.1007.0.0&vd_source=b3d7ff56590244b6e65e38d02a3f101e)；
再之后通过指令拉取rag下载包进行下载，通过上述调整后应用国内镜像源。注意：下载指令变为
'''
docker compose -f docker/docker-compose.yml up -d
'''；
下载完成后检查是否可用，指令：
'''
docker logs -f ragflow-server
'''
若成功则可以通过localhost：80接口本地访问，之后引入本地模型与本地知识库即可。
