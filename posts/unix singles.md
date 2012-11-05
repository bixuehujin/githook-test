---
title: Unix 信号解析
category: Linux
status: published
---

##SIGCHLD## 
当进程终止时由内核发送给终止进程的父进程。父进程处理该信号，用 waitpid 防止僵尸进程的产生。

##SIGKILL##
不可捕捉

##SIGSTOP## 
不可捕捉

SIGPOLL
SIGIO
SIGURG

##SIGPIPE##
当给一个已关闭的 socket 多次发送数据。第一次将收到 RST 响应，第二次收到该信号。该信号的默认处理为终止当前进程。如果要忽略该信号需一下两步：
1.处理 write() 的 EPIPE 错误。
2.使用 signal() 忽略对 SIGPIPE 的默认处理。

## SIG_DFL##

## SIGINT
当在终端中按下中断键（DETETE 或 Control-C）时，有终端驱动发送给所有前台的进程组。

## SIGQUIT

当在终端中按下 Control-backslash 触发该信号


## SIGTSTP

终端控制中，Control-Z 触发该信号

**NOTE**
设置信号处理函数为 SIG_IGN 忽略信号，SIGKILL SIGSTOP 信号不可忽略。

## SIGHUP


## SIGURG



In fact, you should use exit codes only between zero and 127. Exit codes above 128 have
a special meaning—when a process is terminated by a signal, its exit code is 128 plus
the signal number.

