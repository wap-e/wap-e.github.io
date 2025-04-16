### 课后练习

  [习题解答](https://missing-semester-cn.github.io/missing-notes-and-solutions/2020/solutions//course-shell-solution) 本课程中的每节课都包含一系列练习题。有些题目是有明确目的的，另外一些则是开放题，例如“尝试使用 X 和 Y”，我们强烈建议您一定要动手实践，用于尝试这些内容。 此外，我们没有为这些练习题提供答案。如果有任何困难，您可以发送邮件给我们并描述你已经做出的尝试，我们会设法帮您解答。

   本课程需要使用类 Unix shell，例如 Bash 或 ZSH。如果您在 Linux 或者 MacOS 上面完成本课程的练习，则不需要做任何特殊的操作。如果您使用的是 Windows，则您不应该使用 cmd 或是 Powershell；您可以使用 [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/) 或者是 Linux 虚拟机。使用 echo $SHELL 命令可以查看您的 shell 是否满足要求。如果打印结果为 /bin/bash 或 /usr/bin/zsh 则是可以的。

    1.在 /tmp 下新建一个名为 missing 的文件夹。

![Image](https://github.com/user-attachments/assets/a13a4fec-20da-493d-a1d2-ca36d8307029)

    2.用 man 查看程序 touch 的使用手册。

![Image](https://github.com/user-attachments/assets/8df90f2c-c9db-49d2-a253-bb226dd514c1)

    3.用 touch 在 missing 文件夹中新建一个叫 semester 的文件。

touch semester

    4.将以下内容一行一行地写入 semester 文件：

     #!/bin/sh
     curl --head --silent https://missing.csail.mit.edu

    第一行可能有点棘手， # 在 Bash 中表示注释，而 ! 即使被双引号（"）包裹也具有特殊的含义。 单引号（'）则不一样，此处利用这一点解决输入问题。更多信息请参考 [Bash quoting 手册](https://www.gnu.org/software/bash/manual/html_node/Quoting.html)

![Image](https://github.com/user-attachments/assets/a9cbe661-97ff-4527-a761-6c27daf944e1)

    5.尝试执行这个文件。例如，将该脚本的路径（./semester）输入到您的 shell 中并回车。如果程序无法执行，请使用 ls 命令来获取信息并理解其不能执行的原因。

![Image](https://github.com/user-attachments/assets/cb3177bf-e011-4497-9db5-371d0f94b6eb)

    6.查看 chmod 的手册(例如，使用 man chmod 命令)
    7.使用 chmod 命令改变权限，使 ./semester 能够成功执行，不要使用 sh semester 来执行该程序。您的 shell 是如何知晓这个文件需要使用 sh 来解析呢？更多信息请参考：[shebang](https://en.wikipedia.org/wiki/Shebang_(Unix))

![Image](https://github.com/user-attachments/assets/f4db1529-73da-4435-b388-fe0a30c053bb)

    8.使用 | 和 > ，将 semester 文件输出的最后更改日期信息，写入主目录下的 last-modified.txt 的文件中

![Image](https://github.com/user-attachments/assets/6e8049f5-1cda-4d39-8808-0f19c6bdf1c6)

    9写一段命令来从 /sys 中获取笔记本的电量信息，或者台式机 CPU 的温度。注意：macOS 并没有 sysfs，所以 Mac 用户可以跳过这一题。

![Image](https://github.com/user-attachments/assets/60ee2846-7def-4328-8e04-6e023536ea7b)

![Image](https://github.com/user-attachments/assets/cd8c07cd-0ae2-4e31-8198-5e3a804cd50b)
