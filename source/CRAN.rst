=================
CRAN 镜像使用帮助
=================

使用说明
========

在第一次执行 ``install.package("xxx")`` 时会弹出窗口让你选择镜像，此时选择
China Hefei 即可。

也可以通过 ``chooseCRANmirror()`` 来打开窗口，或者 ``options(repos = c(USTC="https://mirrors.ustc.edu.cn/CRAN/"))`` 这个选项来开启USTC镜像。


如果不希望每次打开R都必须选择镜像，可以修改 ``$R_home/library/base/R/Rprofile`` 文件的第(28)行（``$R_home``可以在R中执行``R.home()``得到）：
将

.. code-block:: text

    # options(repos = c(CRAN="@CRAN@"))

替换为

.. code-block:: text

    options(repos = c(USTC="https://mirrors.ustc.edu.cn/CRAN/"))

在Linux系统下，普通用户可能没有 ``$R_home`` 目录的修改权限，此时可以执行

.. code-block:: text

    echo 'options(repos=c(USTC="https://mirrors.ustc.edu.cn/CRAN/"))' >> ~/.Rprofile

以设置当前登录用户的R镜像

相关链接
========

-  官方主页： http://cran.r-project.org/

-  FAQ： http://cran.r-project.org/faqs.html

-  文档： http://cran.r-project.org/doc/
