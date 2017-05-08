## rpms-kubernetes
fork from https://src.fedoraproject.org/cgit/rpms/kubernetes.git 用于生成k8s的rpm的制作

## 步骤
执行命令
1. 修改kubernetes/contrib的包名为kubernetes-commitID, contri-commitID,进行压缩成kubernetes-{commitID}[0:7].tgz/contrib-{commitID}[0:7]
2. 修改kubernetes.spec以及source中的配置信息
3. 安装编译环境依赖的软件包  go/go-bin/go-mdoc
4. 执行rpmbuild -ba kubernetes.spec
[注意]
chroot /media/
mount --bind /dev /media/dev 
cd /media/root/rpmbuild/SOURCE/
执行rpmbuild -ba kubernetes.spec

