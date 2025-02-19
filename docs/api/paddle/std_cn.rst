.. _cn_api_tensor_cn_std:

std
-------------------------------

.. py:function:: paddle.std(x, axis=None, unbiased=True, keepdim=False, name=None)

沿给定的轴 ``axis`` 计算 ``x`` 中元素的标准差。

参数
::::::::::
   - x (Tensor) - 输入的Tensor，数据类型为：float32、float64。
   - axis (int|list|tuple，可选) - 指定对 ``x`` 进行计算的轴。``axis`` 可以是int、list(int)、tuple(int)。如果 ``axis`` 包含多个维度，则沿着 ``axis`` 中的所有轴进行计算。``axis`` 或者其中的元素值应该在范围[-D, D)内，D是 ``x`` 的维度。如果 ``axis`` 或者其中的元素值小于0，则等价于 :math:`axis + D`。如果 ``axis`` 是None，则对 ``x`` 的全部元素计算标准差。默认值为None。
   - unbiased (bool，可选) - 是否使用无偏估计来计算标准差。使用 :math:`N` 来代表在 axis 上的维度，如果 ``unbiased`` 为True，则在计算中使用 :math:`N - 1` 作为除数。为 False 时将使用 :math:`N` 作为除数。默认值为True。
   - keepdim (bool，可选) - 是否在输出Tensor中保留减小的维度。如果 ``keepdim`` 为True，则输出Tensor和 ``x`` 具有相同的维度(减少的维度除外，减少的维度的大小为1)。否则，输出Tensor的形状会在 ``axis`` 上进行squeeze操作。默认值为False。
   - **name** (str，可选) - 具体用法请参见 :ref:`api_guide_Name`，一般无需设置，默认值为 None。

返回
::::::::::
    ``Tensor``，沿着 ``axis`` 进行标准差计算的结果，数据类型和 ``x`` 相同。

代码示例
::::::::::

COPY-FROM: paddle.std