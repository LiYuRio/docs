.. _cn_api_nn_ELU:

ELU
-------------------------------
.. py:class:: paddle.nn.ELU(alpha=1.0, name=None)

ELU激活层（ELU Activation Operator）

根据 `Exponential Linear Units <https://arxiv.org/abs/1511.07289>`_ 对输入Tensor中每个元素应用以下计算。

.. math::

    ELU(x)=
        \left\{
            \begin{array}{lcl}
            x,& &\text{if } \ x > 0 \\
            alpha * (e^{x} - 1),& &\text{if } \ x <= 0
            \end{array}
        \right.

其中，:math:`x` 为输入的 Tensor

参数
::::::::::
    - alpha (float，可选) - ELU的alpha值，默认值为1.0。
    - **name** (str，可选) - 具体用法请参见 :ref:`api_guide_Name`，一般无需设置，默认值为 None。

形状：
::::::::::
    - input：任意形状的Tensor。
    - output：和input具有相同形状的Tensor。

代码示例
:::::::::

COPY-FROM: paddle.nn.ELU