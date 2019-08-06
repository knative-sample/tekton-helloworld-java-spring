# tekton-knative-java-spring helloworld
tekton knative for java helloworld 

本示例有两个 Task, 分别负责：从源码编译成镜像以及把镜像发布成 Knative Service. 下面分别说一下这两个 Task
- 从源码编译成镜像
需要给定 gitRepo 参数，并通过此参数 clone 代码, step 2 通过 clone 下来的代码直接使用 Kaniko 编译成镜像，并推送到镜像仓库
- 把镜像发布成 Knative Service
和 Task 1 一样需要 clone 代码，然后从代码中指定的 yaml 文件发布成 Knative 的 Service


