## 相关组织与标准
### ISO C
**ISO C的意图是提供C的可移植性，使其能适合于大量不同的操作系统，而不只是适合UNIX系统**
*ANSI*: 美国国家标准学会（American National Standards Institute）
*ISO*：国际标准化组织（International Organization for Standardization）
*IEC*：国际电子技术委员会（International Electrotechnical Commission）
* ANSI是ISO中代表美国的成员。
* 1989年发布的版本称为C89
* 1999年发布的版本称为C99。改善了对进行数值处理的应用软件的支持，并对函数原型增加了关键字`restict`。它告诉编译器，哪些指针引用是可以优化的，其方法是指出指针引用的对象在函数中通过该指针进行访问
* 2011年发布的版本称为C11。
> TODO: 补充C的版本说明

### IEEE POSIX
**POSIX的意图是提升应用程序在各种UNIX系统环境之间的可移植性**
*IEEE*：电气和电子工程师学会（Institute of Electrical and Electronics Engineers）
*POSIX*：可移植操作系统接口（Portable Operating System Interface）
* POSIX说明的是一个接口而不是一种实现，所以并不区分系统调用和库函数
* 1989年发布的POSIX.1指的是IEEE 1003.1-1990，也等于ISO/IEC 9945-1:1990
* 1996年发布修订版：IEEE 1003.1-1996。新增了==实时扩展标准==以及==pthreads多线程编程接口==。
* 1999年发布IEEE 1003.1d-1999。增加许多高级实时扩展
* 2000年发布IEEE 1003.1j-2000。增加更多高级实时扩展
* 2000年发布IEEE 1003.1q-2000。增加==标准在事件跟踪方面的扩展==
* 后续的版本还包括：协议无关接口、shell及实用程序的修正、批处理扩展、网络服务等等

### SUS
SUS是POSIX的一个超集。
SUS：单一UNIX规范(Single UNIX Specification)
只有厂商实现了SUS规定的一系列接口才能称为UNIX系统

### ISO C标准定义的头文件
| 文件名          | FreeBSD 8.0 | Linux 3.2.0 | MacOS X 10.6.8 | Solaris 10 | 说明           |
| :----------- | :---------: | :---------: | :------------: | :--------: | :----------- |
| <assert.h>   |      ✅      |      ✅      |       ✅        |     ✅      | 验证程序断言       |
| <complex.h>  |      ✅      |      ✅      |       ✅        |     ✅      | 复数算术运算支持     |
| <ctype.h>    |      ✅      |      ✅      |       ✅        |     ✅      | 字符分类和映射支持    |
| <errno.h>    |      ✅      |      ✅      |       ✅        |     ✅      | 出错码          |
| <fenv.h>     |      ✅      |      ✅      |       ✅        |     ✅      | 浮点环境         |
| <float.h>    |      ✅      |      ✅      |       ✅        |     ✅      | 浮点常量及特征      |
| <inttypes.h> |      ✅      |      ✅      |       ✅        |     ✅      | 整型格式变化       |
| <iso646.h>   |      ✅      |      ✅      |       ✅        |     ✅      | 赋值、关系及一元操作符宏 |
| <limits.h>   |      ✅      |      ✅      |       ✅        |     ✅      | 实现变量         |
| <locale.h>   |      ✅      |      ✅      |       ✅        |     ✅      | 本地话类别及相关定义   |
| <math.h>     |      ✅      |      ✅      |       ✅        |     ✅      | 数学函数、类型声明及常量 |
| <setjmp.h>   |      ✅      |      ✅      |       ✅        |     ✅      | 非局部goto      |
| <signal.h>   |      ✅      |      ✅      |       ✅        |     ✅      | 信号           |
| <stdarg.h>   |      ✅      |      ✅      |       ✅        |     ✅      | 可变参数         |
| <stdbool.h>  |      ✅      |      ✅      |       ✅        |     ✅      | 布尔类型和值       |
| <stddef.h>   |      ✅      |      ✅      |       ✅        |     ✅      | 标准定义         |
| <stdint.h>   |      ✅      |      ✅      |       ✅        |     ✅      | 整型           |
| <stdio.h>    |      ✅      |      ✅      |       ✅        |     ✅      | 标准I/O库       |
| <stdlib.h>   |      ✅      |      ✅      |       ✅        |     ✅      | 使用函数         |
| <string.h>   |      ✅      |      ✅      |       ✅        |     ✅      | 字符串操作        |
| <tgmath.h>   |      ✅      |      ✅      |       ✅        |     ✅      | 通用类型数学函数     |
| <time.h>     |      ✅      |      ✅      |       ✅        |     ✅      | 时间和日期        |
| <wchar.h>    |      ✅      |      ✅      |       ✅        |     ✅      | 扩充的多字节和宽字符支持 |
| <wctype.h>   |      ✅      |      ✅      |       ✅        |     ✅      | 宽字符和映射支持     |
### POSIX.1指定的头文件
POSIX标准的头文件包含必选和可选两部分。同时POSIX还包含[[#ISO C标准定义的头文件]]
#### 必选的头文件
| 文件名             | FreeBSE 8.0 | Linux 3.2.0 | MacOS X 10.6.8 | Solaris 10 | 说明         |
| :-------------- | :---------: | :---------: | :------------: | :--------: | :--------- |
| <aio.h>         |      ✅      |      ✅      |       ✅        |     ✅      | 异步I/O      |
| <cpio.h>        |      ✅      |      ✅      |       ✅        |     ✅      | cpio归档值    |
| <dirent.h>      |      ✅      |      ✅      |       ✅        |     ✅      | 目录项        |
| <dlfcn.h>       |      ✅      |      ✅      |       ✅        |     ✅      | 动态链接       |
| <fcntl.h>       |      ✅      |      ✅      |       ✅        |     ✅      | 文件控制       |
| <fnmatch.h>     |      ✅      |      ✅      |       ✅        |     ✅      | 文件名匹配类型    |
| <glob.h>        |      ✅      |      ✅      |       ✅        |     ✅      | 路径名模式匹配与生成 |
| <grp.h>         |      ✅      |      ✅      |       ✅        |     ✅      | 组文件        |
| <iconv.h>       |      ✅      |      ✅      |       ✅        |     ✅      | 代码集变换使用程序  |
| <langinfo.h>    |      ✅      |      ✅      |       ✅        |     ✅      | 语言信息常量     |
| <monetary.h>    |      ✅      |      ✅      |       ✅        |     ✅      | 货币类型与函数    |
| <netdb.h>       |      ✅      |      ✅      |       ✅        |     ✅      | 网络数据库操作    |
| <nl_types.h>    |      ✅      |      ✅      |       ✅        |     ✅      | 消息类        |
| <poll.h>        |      ✅      |      ✅      |       ✅        |     ✅      | 投票函数       |
| <pthread.h>     |      ✅      |      ✅      |       ✅        |     ✅      | 线程         |
| <pwd.h>         |      ✅      |      ✅      |       ✅        |     ✅      | 口令文件       |
| <regex.h>       |      ✅      |      ✅      |       ✅        |     ✅      | 正则表达式      |
| <sched.h>       |      ✅      |      ✅      |       ✅        |     ✅      | 执行调度       |
| <semaphore.h>   |      ✅      |      ✅      |       ✅        |     ✅      | 信号量        |
| <strings.h>     |      ✅      |      ✅      |       ✅        |     ✅      | 字符串操作      |
| <tar.h>         |      ✅      |      ✅      |       ✅        |     ✅      | tar归档值     |
| <termios.h>     |      ✅      |      ✅      |       ✅        |     ✅      | 终端I/O      |
| <unistd.h>      |      ✅      |      ✅      |       ✅        |     ✅      | 符号常量       |
| <wordexp.h>     |      ✅      |      ✅      |       ✅        |     ✅      | 字扩充类型      |
| <arpa/inet.h>   |      ✅      |      ✅      |       ✅        |     ✅      | 因特网定义      |
| <net/if.h>      |      ✅      |      ✅      |       ✅        |     ✅      | 套接字本地接口    |
| <netinet/in.h>  |      ✅      |      ✅      |       ✅        |     ✅      | 因特网地址族     |
| <netinet/tcp.h> |      ✅      |      ✅      |       ✅        |     ✅      | 传输控制协议定义   |
| <sys/mman.h>    |      ✅      |      ✅      |       ✅        |     ✅      | 存储管理声明     |
| <sys/select.h>  |      ✅      |      ✅      |       ✅        |     ✅      | select函数   |
| <sys/socket.h>  |      ✅      |      ✅      |       ✅        |     ✅      | 套接字接口      |
| <sys/stat.h>    |      ✅      |      ✅      |       ✅        |     ✅      | 文件状态       |
| <sys/statvfs.h> |      ✅      |      ✅      |       ✅        |     ✅      | 文件系统信息     |
| <sys/times.h>   |      ✅      |      ✅      |       ✅        |     ✅      | 进程时间       |
| <sys/tyeps.h>   |      ✅      |      ✅      |       ✅        |     ✅      | 基本系统数据类型   |
| <sys/un.h>      |      ✅      |      ✅      |       ✅        |     ✅      | UNIX域套接字定义 |
| <sys/utsname.h> |      ✅      |      ✅      |       ✅        |     ✅      | 系统名        |
| <sys/wait.h>    |      ✅      |      ✅      |       ✅        |     ✅      | 进程控制       |
#### 可选头文件
| 文件名              | FreeBSE 8.0 | Linux 3.2.0 | MacOS X 10.6.8 | Solaris 10 | 说明        |
| :--------------- | :---------: | :---------: | :------------: | :--------: | :-------- |
| <fmtmsg.h>       |      ✅      |      ✅      |       ✅        |     ✅      | 消息显示结构    |
| <ftw.h>          |      ✅      |      ✅      |       ✅        |     ✅      | 文件树漫游     |
| <libgen.h>       |      ✅      |      ✅      |       ✅        |     ✅      | 路径名管理函数   |
| <ndbm.h>         |      ✅      |      ❌      |       ✅        |     ✅      | 数据库操作     |
| <search.h>       |      ✅      |      ✅      |       ✅        |     ✅      | 搜索表       |
| <syslog.h>       |      ✅      |      ✅      |       ✅        |     ✅      | 系统出错日志记录  |
| <utmpx.h>        |      ✅      |      ✅      |       ✅        |     ✅      | 用户账户数据库   |
| <sys/ipc.h>      |      ✅      |      ✅      |       ✅        |     ✅      | IPC       |
| <sys/msg.h>      |      ✅      |      ✅      |       ✅        |     ✅      | XSI消息队列   |
| <sys/resource.h> |      ✅      |      ✅      |       ✅        |     ✅      | 资源操作      |
| <sys/sem.h>      |      ✅      |      ✅      |       ✅        |     ✅      | XSI信号量    |
| <sys/shm.h>      |      ✅      |      ✅      |       ✅        |     ✅      | XSI共享存储   |
| <sys/time.h>     |      ✅      |      ✅      |       ✅        |     ✅      | 时间类型      |
| <sys/uio.h>      |      ✅      |      ✅      |       ✅        |     ✅      | 矢量I/O操作   |
| <mqueue.h>       |      ✅      |      ✅      |       ❌        |     ✅      | 消息队列      |
| <spawn.h>        |      ✅      |      ✅      |       ✅        |     ✅      | 实时spawn接口 |
#### 可选接口组和选项码
定义在`<unistd.h>`中

| 选项码 | SUS强制的 | 符号常量                               | 说明               |
| :-: | :----: | :--------------------------------- | :--------------- |
| ADV |        | \_POSIX_ADVISORY_INFO              | 建议性信息（实时）        |
| CPT |        | \_POSIX_CPUTIME                    | 进程CPUT时间时钟（实时）   |
| FSC |   ✅    | \_POSIX_FSYNC                      | 文件同步             |
| IP6 |        | \_POSIX_IPV6                       | IPv6接口           |
| ML  |        | \_POSIX_MEMLOCK                    | 进程存储区加锁（实时）      |
| MLR |        | \_POSIX_MEMLOCK_RANGE              | 存储区域加锁（实时）       |
| MON |        | \_POSIX_MONOTONIC_CLOCK            | 单调时钟（实时）         |
| MSG |        | \_POSIX_MESSAGE_PASSING            | 消息传送（实时）         |
| MX  |        | \_\_STDC_IEC_599__                 | IEC 60559浮点选项    |
| PIO |        | \_POSIX_PRIORITIZED_IO             | 优先输入和输出          |
| PS  |        | \_POSIX_PRIORITIZED_SCHEDULING     | 进程调度（实时）         |
| RPI |        | \_POSIX_THREAD_ROBUST_PRIO_INHERIT | 健壮的互斥量优先权继承（实时）  |
| RPP |        | \_POSIX_THREAD_ROBUST_PRIO_PROTECT | 健壮的互斥量优先权保护（实时）  |
| RS  |        | \_POSIX_RAW_SOCKETS                | 原始套接字            |
| SHM |        | \_POSIX_SHARED_MEMORY_OBJECTS      | 共享存储对象（实时）       |
| SIO |        | \_POSIX_SYNCHRONIZED_IO            | 同步输入和输出（实时）      |
| SPN |        | \_POSIX_SPAWN                      | 产生（实时）           |
| SS  |        | \_POSIX_SPORADIC_SERVER            | 进程阵发性服务器（实时）     |
| TCT |        | \_POSIX_THREAD_CPUTIME             | 线程CPU时间时钟（实时）    |
| TPI |        | \_POSIX_THREAD_PRIO_INHERIT        | 非健壮的互斥量优先权继承（实时） |
| TPP |        | \_POSIX_THREAD_PRIO_PROTECT        | 非健壮的互斥量优先权保护（实时） |
| TPS |        | \_POSIX_THREAD_PRIORITY_SCHEDULING | 线程执行调度（实时）       |
| TSA |   ✅    | \_POSIX_THREAD_ATTR_STACKADDR      | 线程栈地址属性          |
| TSS |   ✅    | \_POSIX_THREAD_ATTR_STACKSIZE      | 线程栈长度属性          |
| TSH |   ✅    | \_POSIX_THREAD_PROCESS_SHARED      | 线程进程共享同步         |
| TSP |        | \_POSIX_THREAD_SPORADIC_SERVER     | 线程阵发性服务器（实时）     |
| TYM |        | \_POSIX_TYPED_MEMORY_OBJECTS       | 类型存储对象（实时）       |
| XSI |   ✅    | \_XOPEN_UNIX                       | X/Open扩充接口       |
## 限制
UNIX系统实现定义了很多幻数和常量，其中有很多已经被硬编码到程序中，还有一些可以特定的技术确定。
两种必须的限制：
* 编译时限制: 定义在头文件中的一些值，只要在编译时包含这些头文件就可以获取
* 运行时限制：需要根据程序执行时的环境来确认的限制。比如程序可能运行在不同的文件系统中，各种文件系统对于文件名的长度限制时不一样的。
为了获取这两种限制的值，有三种方法：
1. 编译时限制（定义在同文件中）
2. 与文件或目录*无*关的运行时限制（用sysconf函数获取）
3. 与文件或目录*有*关的运行时限制（用pathconf和fpathconf函数获取）
### ISO C限制
整数相关的限制定义在`<limits.h>`中
浮点数相关的限制定义在`<float.h>`中
在`<stdio.h>`中还定义了几个常量:
* `FOPEN_MAX`常量，表示进程同时可以打开的标准I/O流的最小个数
* `TMP_MAX`常量，由`tmpnam`函数产生的唯一文件名的最大个数
* `FILENAME_MAX`常量，尽量避免使用。用`NAME_MAX`和 `PATH_MAX`两个常量替代

### POSIX限制
POSIX限制分为7类：
1. 数值限制：LONG_BIT、SSIZE_MAX和WORD_BIT
2. [[#最小值]]：定义在`<limits.h>`中，以`_POSIX_`开头的值
3. 最大值：\_POSIX_CLOCKRES_MIN
4. 运行时可以增加的值：CHARCLASS_NAME_MAX、COLL_WEIGHTS_MAX、LING_MAX、NGROUPS_MAX和RE_DUP_MAX
5. [[#运行时不变的值]]
6. 其他不变值：NL_ARGMAX、NL_MSGMAX、NL_SETMAX和NL_TEXTMAX
7. 路径名可变值：FILESIZEBITS、LINK_MAX、MAX_CANON、MAX_INPUT、NAME_MAX、PATH_MAX、PIPE_BUF和SYMLINK_MAX
#### 最小值
下表中的值是由POSIX设置的最低限度。如果要获取各实现设定这值，只需要去掉`_POSIX_`前缀即可

| 名称                     | 说明                                              |
| :--------------------- | :---------------------------------------------- |
| \_POSIX_ARG_MAX        | exec函数的参数长度                                     |
| \_POSIX_CHILD_MAX      | 每个实际用户ID的子进程数                                   |
| \_POSIX_DELAYTIMER_MAX | 定时器最大超限运行次数                                     |
| \_POSIX_HOST_NAME_MAX  | `gethostname`函数返回的主机名长度                         |
| \_POSIX_LINK_MAX       | 到一个文件的链接数                                       |
| \_POSIX_LOGIN_NAME_MAX | 登录名的长度                                          |
| \_POSIX_MAX_CANON      | 终端规范输入队列的字节数                                    |
| \_POSIX_MAX_INPUT      | 终端输入队列的可用空间                                     |
| \_POSIX_NAME_MAX       | 文件名的字节数，不包括null字符                               |
| \_POSIX_NGROUPS_MAX    | 每个进程同时添加的组ID数                                   |
| \_POSIX_OPEND_MAX      | 每个进程的打开文件数                                      |
| \_POSIX_PATH_MAX       | 路径名中的字节数，包括null字符                               |
| \_POSIX_PIPE_BUF       | 能原子地写到一个管道中的字节数                                 |
| \_POSIX_RE_DUP_MAX     | 当使用间隔表示法时，`regexec`和`regcomp`函数允许的基本正则表达式重复发生次数 |
| \_POSIX_RTSIG_MAX      | 为应用预留的实时信号编号个数                                  |
| \_POSIX_SEM_NSEMS_MAX  | 一个进程可以同时使用的信号量个数                                |
| \_POSIX_SEM_VALUE_MAX  | 信号量可持有的值                                        |
| \_POSIX_SIGQUEUE_MAX   | 一个进程可发送和刮起的排队信号的个数                              |
| \_POSIX_SSIZE_MAX      | 能存在ssize_t对象中的值                                 |
| \_POSIX_STREAM_MAX     | 一个进程能同时打开的标准I/O流个数                              |
| \_POSIX_SYMLINK_MAX    | 符号链接中的字节数                                       |
| \_POSIX_SYMLOOP_MAX    | 在解析路径名时，可遍历的符号链接数                               |
| \_POSIX_TIMER_MAX      | 每个进程的定时器数目                                      |
| \_POSIX_TTY_NAME_MAX   | 终端设备名长度，包括null符                                 |
| \_POSIX_TZNAME_MAX     | 时区名字节数                                          |
#### 运行时不变的值
| 名称             | 说明                      |
| :------------- | :---------------------- |
| ARG_MAX        | exec函数族的参数最大长度          |
| ATEXIT_MAX     | 可用`atexit`函数登记的最大函数个数   |
| CHILD_MAX      | 每个实际用户ID的子进程个数          |
| DELAYTIMER_MAX | 定时器最大超限运行次数             |
| HOST_NAME_MAX  | `gethostname`函数返回的主机名长度 |
| LOGIN_NAME_MAX | 登录名最大长度                 |
| OPEN_MAX       | 赋予新建文件描述符的最大值+1         |
| PAGESIZE       | 系统内存页大小（以字节为大小）         |
| RTSIG_MAX      | 为应用程序预留的实时限号的最大个数       |
| SEM_NSEMS_MAX  | 一个进程可使用的信号量最大个数         |
| SEM_VALUE_MAX  | 信号量的最大值                 |
| SIGQUEUE_MAX   | 一个进程可排队信号的最大个数          |
| STREAM_MAX     | 一个进程一次可打开的标准I/O流的最大个数   |
| SYMLOOP_MAX    | 路径解析过程中可访问的符号链接数        |
| TIMER_MAX      | 一个进程的定时器最大个数            |
| TTY_NAME_MAX   | 终端设备名长度，包括null字符        |
| TZNAME_MAX     | 时区名的字节数                 |
### XSI限制
最常用的限制是`NZERO`：默认进程优先级

### 获取运行时限制的函数
```c
#include <unistd.h>
long sysconf(int name);
long pathconf(const char* pathname, int name);
long fpathconf(int fd, int name);
```
对于返回值的说明：
1. 如果name参数并不是一个合适的常量，3个函数都返回-1，并把`errno`设置为`EINVAL`
2. 有些name会返回一个变量值或提示改值是不确定的。不确定的值用-1表示，但不会修改errno值
#### `sysconf`函数name参数的可选值：

| 限制名              | 说明                                 | name参数                |
| :--------------- | :--------------------------------- | :-------------------- |
| ARG_MAX          | exec函数参数的最大长度(字节)                  | \_SC_ARG_MAX          |
| ATEXIT_MAX       | 可用`atexit`函数登记的最大函数个数              | \_SC_ATEXIT_MAX       |
| CHILD_MAX        | 每个实际用户ID的子进程个数                     | \_SC_CHILD_MAX        |
|                  | 时钟滴答/秒                             | \_SC_CLK_TCK          |
| COLL_WEIGHTS_MAX | 在本地定义文件中可以赋予LC_COLLATE顺序关键字项的最大权重数 | \_SC_COLL_WEIGHTS_MAX |
| DELAYTIMER_MAX   | 定时器最大超限运行次数                        | \_SC_DELAYTIMER_MAX   |
| HOST_NAME_MAX    | `gethostname`函数返回的主机名最大长度          | \_SC_HOST_NAME_MAX    |
| IOV_MAX          | readv或writev函数可以使用最多的iovec结构的个数    | \_SC_IOV_MAX          |
| LINE_MAX         | 使用程序输入行的最大长度                       | \_SC_LINE_MAX         |
| LOGIN_NAME_MAX   | 登录名的最大长度                           | \_SC_LOGIN_NAME_MAX   |
| NGROUPS_MAX      | 每个进程同时添加的最大进程组ID数                  | \_SC_NGROUPS_MAX      |
| OPEN_MAX         | 每个进程最大打开文件数                        | \_SC_OPEN_MAX         |
| PAGESIZE         | 系统存储也长度(字节数)                       | \_SC_PAGESIZE         |
| PAGE_SIZE        | 系统存储也长度(字节数)                       | \_SC__MAX             |
| RE_DUP_MAX       |                                    | \_SC_RE_DUP_MAX       |
| RTSIG_MAX        | 为应用程序预留的实时信号的最大个数                  | \_SC_RTSIG_MAX        |
| SEM_NSEMS_MAX    | 一个进程可使用的信号量最大个数                    | \_SC_SEM_NSEMS_MAX    |
| SEM_VALUE_MAX    | 信号量的最大值                            | \_SC_SEM_VALUE_MAX    |
| SIGQUEUE_MAX     | 一个进程可排队信号的最大个数                     | \_SC_SIGQUEUE_MAX     |
| STREAM_MAX       | 进程在任意给定时刻标准I/O流的最大个数               | \_SC_STREAM_MAX       |
| SYMLOOP_MAX      | 在解析路径名时，可遍历的符号链接数                  | \_SC_SYMLOOP_MAX      |
| TIMER_MAX        | 每个进程的最大定时器个数                       | \_SC_TIMER_MAX        |
| TTY_NAME_MAX     | 终端设备名长度，包含null字节                   | \_SC_TTY_NAME_MAX     |
| TZNAME_MAX<br>   | 时区名的最大字节数                          | \_SC_TZNAME_MAX       |
#### `pathconf`和`fpathconf`函数的name参数可选值

| 限制名                          | 说明                       | name参数                    | 对pathname和fd参数的限制              |
| :--------------------------- | :----------------------- | :------------------------ | ------------------------------ |
| FILESIZEBITS                 | 制定目录中允许的普通文件最大长度所需要的最小位数 | \_PC_FILESIZEBITS         | 文件必须是目录，返回的值用于改目录中的文件名         |
| LINK_MAX                     | 文件链接技术的最大值               | \_PC_LINK_MAX             | 如果文件是目录，则返回值用于目录本身，而不是目录内的文件名项 |
| MAX_CANON                    | 终端规范输入队列的最大字节数           | \_PC_MAX_CANON            | 文件必须输出终端文件                     |
| MAX_INPUT                    | 终端输入队列可用空间的字节数           | \_PC_MAX_INPUT            |                                |
| NAME_MAX                     | 文件名的最大字节数，不包括null字节      | \_PC_NAME_MAX             | 文件必须是目录，返回的值用于改目录中的文件名         |
| PATH_MAX                     | 相对路径名的最大字节数，包括null字节     | \_PC_PATH_MAX             | 文件必须是目录。如果是相对路径时，返回的相对路径名的最大长度 |
| PIPE_BUF                     | 能原子地写到管道的最大字节数           | \_PC_PIPE_BUF             | 文件必须是管道、FIFO或目录                |
| \_POSIX_TIMESTAMP_RESOLUTION | 文件时间戳的纳秒精度               | \_PC_TIMESTAMP_RESOLUTION | 如果文件是目录，则返回值用于目录本身，而不是目录内的文件名项 |
| SYMLINK_MAX                  | 符号链接的字节数                 | \_PC_SYMLINK_MAX          |                                |

## 基本系统数据类型
定义在`<sys/types.h>`文件中

| 类型           | 说明               |
| :----------- | :--------------- |
| clock_t      | 时钟滴答计数器          |
| comp_t       | 压缩的时钟滴答          |
| dev_t        | 设备号(主和次)         |
| fd_set       | 文件描述符集           |
| fpost_t      | 文件位置             |
| gid_t        | 数值组ID            |
| ino_t        | i节点编号            |
| mode_t       | 文件类型，文件创建模式      |
| nlink_t      | 目录项的链接计数         |
| off_t        | 文件长度和偏移量(带符号的)   |
| pid_t        | 进程ID和进程组ID(带符号的) |
| pthread_t    | 线程ID             |
| ptrdiff_t    | 两个指针相减的结果(带符号的)  |
| rlim_t       | 资源限制             |
| sig_atomic_t | 能原子性访问的数据类型      |
| sigset_      | 信号集              |
| size_t       | 对象长度(不带符号的)      |
| ssize_t      | 返回字节计数的函数(带符号的)  |
| time_t       | 日历事件的秒计数器        |
| uid_t        | 数值用户ID           |
| wchar_t      | 能表示所有不同的字符码      |
