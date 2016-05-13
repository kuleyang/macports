# MacPorts - 本地仓库

为MacPorts构建的本地仓库。

## 安装

1. 根据你的Mac OS X版本[安装 MacPorts](https://www.macports.org/install.php)。

2. 克隆此仓库，并建立索引。


        $ sudo -u macports git clone https://github.com/kuleyang/macports.git /opt/local/macports
        $ cd /opt/local/macports
        $ portindex

3. 编辑sources.conf

        $ sudo vi /opt/local/etc/macports/sources.conf

4. 增加 `file:///opt/local/macports`  **在"rsync://rsync.macports.org/"这一行之前**。 T

5. 从此仓库安装。

        $ sudo port install webkit2png


## 问题

	Error: Unable to execute port: Could not open file
	
解决：

	sudo vi /opt/local/etc/macports/macports.conf

增加一行：

	macportsuser       macports