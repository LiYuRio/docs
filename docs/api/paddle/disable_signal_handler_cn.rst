.. _cn_api_fluid_disable_signal_handler:

disable_signal_handler
-------------------------------

.. py:function:: paddle.disable_signal_handler()

关闭Paddle系统信号处理方法

Paddle默认在C++层面注册了系统信号处理方法，用于优化报错信息。
但是一些特定的Python module可能需要使用某些系统信号，引发冲突。
您可以通过调用本函数来关闭Paddle的系统信号处理方法

如果您在一个Python文件中同时使用了Paddle和下述框架的一种或多种，
则请在其他框架执行前首先调用paddle.disable_signal_handler()

1.TVM框架
2.ADLIK框架

返回
:::::::::
无

代码示例
:::::::::

COPY-FROM: paddle.disable_signal_handler