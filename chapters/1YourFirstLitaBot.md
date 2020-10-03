<h1 id="1.1">运行环境</h1>

一个严峻的事实: Ruby 生态系统首先瞄准了 linux，其次是 macOS，而 Windows 则排在第三。

Windows用户可以使用VMware虚拟机创建linux系统环境，Windows 10用户还有另一个选择，安装Windows Subsystem for Linux（WSL）,详见[官方文档](https://docs.microsoft.com/en-us/windows/wsl/install-win10)。

> 本书中的例子都是针对Ubuntu编写和测试的，所以如果你对使用其他的Linux发行版没有强烈的需求，最好从Ubuntu开始。

本文测试的是[VMware](https://www.vmware.com/cn/products/workstation-pro/workstation-pro-evaluation.html)版本是VMware Workstation Pro 15.1.0，[Ubuntu](https://cn.ubuntu.com/download) 版本是 Ubuntu 20.04 LTS 版本。

[安装教程](https://www.linuxidc.com/Linux/2020-03/162547.htm)

**安装Ruby**

```bash
sudo apt-get install ruby
```

**查看已安装的Ruby、gem和Bundler版本**

```bash
$ ruby --version
ruby 2.7.0p0 (2019-12-25 revision 647ee6f091) [x86_64-linux-gnu]
$ gem --version
3.1.2
$ bundle --version

Command 'bundle' not found, but can be installed with:

sudo snap install ruby          # version 2.7.1, or
sudo apt  install ruby-bundler  # version 2.1.4-1

See 'snap info ruby' for additional versions.

```

出现查询不到`bundle`命令的错误，根据提示使用`sudo apt  install ruby-bundler`来安装Bundler

```bash
$ bundle --version
Bundler version 2.1.4
```



> 注：原文是使用`gem install bundler`来安装，这里没有测试

我们需要gem和Bundler来安装Lita和它的Ruby依赖。

