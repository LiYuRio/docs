.. _cn_api_linalg_inv:

inv
-------------------------------

.. py:function:: paddle.linalg.inv(x, name=None)


计算方阵的逆。方阵是行数和列数相等的矩阵。输入可以是一个方阵（2-D张量），或者是批次方阵（维数大于2时）。

参数
:::::::::
  - **x** (Tensor) – 输入张量，最后两维的大小必须相等。如果输入张量的维数大于2，则被视为2-D矩阵的批次（batch）。支持的数据类型：float32，float64。
  - **name** (str，可选) - 具体用法请参见 :ref:`api_guide_Name`，一般无需设置，默认值为 None。

返回
::::::::
Tensor，输入方阵的逆。


代码示例
:::::::::

COPY-FROM: paddle.linalg.inv