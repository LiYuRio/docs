.. _cn_api_tensor_add:

add
-------------------------------

.. py:function:: paddle.add(x, y, name=None)



逐元素相加算子，输入 ``x`` 与输入 ``y`` 逐元素相加，并将各个位置的输出元素保存到返回结果中。

输入 ``x`` 与输入 ``y`` 必须可以广播为相同形状，关于广播规则，请参考 :ref:`cn_user_guide_broadcasting`

等式为：

.. math::
        Out = X + Y

- :math:`X`：多维Tensor。
- :math:`Y`：多维Tensor。

参数
:::::::::
    - x (Tensor) - 输入的Tensor，数据类型为：float32、float64、int32、int64。
    - y (Tensor) - 输入的Tensor，数据类型为：float32、float64、int32、int64。
    - **name** (str，可选) - 具体用法请参见 :ref:`api_guide_Name`，一般无需设置，默认值为 None。

返回
:::::::::
多维Tensor，数据类型与 ``x`` 相同，维度为广播后的形状。


代码示例
:::::::::

COPY-FROM: paddle.add