# k8s-config-split
## 解析kubectl的config文件, 生成ca.crt, client.crt和client.key文件.
## 用法: python k2file.py /etc/kubernetes/admin.conf

## 有个问题: script_dir 总是获取 k2file.py 脚本所在的目录, 而非执行脚本所在的目录.
## 而使用 open() 打开并创建文件时, 如果不写绝对路径, 就会使用以脚本所在位置的相对路径.
## 需要使用 os.getcwd() 代替, 这样得到的是执行脚本时所在的目录, 而非脚本本身所在的目录.


## python2内置yaml模块, python3则需要使用pip安装PyYAML
