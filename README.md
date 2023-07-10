内核

	make
 
	insmod netlinkKo.ko

用户

	gcc netlinkUsr.c -o netlinkUsr
 
	./netlinkUsr

其他

	demsg 查看内核模块安装情况
 
	cat /proc/sys/kernel/tainted 观察内核污染情况
 
	for i in $(seq 18); do  echo $(($i-1)) $(($(cat /proc/sys/kernel/tainted)>>($i-1)&1)); done;
