# 启动项目

我本就是是一个不走寻常路的人，因此我需要在1个月内学会c++，并最起码能用c++来实现 一个网站，因此凭感悟来吧

首先我需要一个编译器，目前来看我知道的就是gcc和g++了，暂时搞不清他们之间的关系，我就知道一点g++可以用来编译*.cc的文件，gcc可以用来编译*.c的文件

* 第一步确认我已经安装了g++
* 第二步写一个文件hello.cc内容如下

```c++
  #include <iostream>
  using namespace std;
  int main()
  {
      cout << "Hello, world!" << endl;
      return 0;
  }
```

* 编译

```shell
g++ hello.cc  -o hello.out
```

* 执行

```shell
./hello.out
```

输出：Hello, world!