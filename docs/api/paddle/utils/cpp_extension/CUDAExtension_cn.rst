.. _cn_api_paddle_utils_cpp_extension_CUDAExtension:

CUDAExtension
-------------------------------

.. py:function:: paddle.utils.cpp_extension.CUDAExtension(sources, *args, **kwargs)

此接口用于配置自定义 OP 的源文件信息，编译生成同时支持 CPU 和 GPU 设备上执行的算子。若要编译仅支持 CPU 设备的算子，请使用 :ref:`cn_api_paddle_utils_cpp_extension_CppExtension` 。

此接口是对 Python 内建库 ``setuptools.Extension`` 的进一步封装。除了不需要显式地指定 ``name`` 参数，其他参数以及使用方式上，与原生内建库接口保持一致。

**使用样例如下：**

.. code-block:: text

    # setup.py 

    # 编译支持 CPU/GPU 的算子
    from paddle.utils.cpp_extension import CUDAExtension, setup

    setup(
        name='custom_op',
        ext_modules=CUDAExtension(
            sources=['relu_op.cc', 'relu_op.cu']
        )
    )



.. note::

    搭配 ``setup`` 接口使用，编译生成的动态库名称与 :ref:`cn_api_paddle_utils_cpp_extension_setup` 接口中的 ``name`` 一致。



参数
::::::::::::

  - **sources** (list[str]) - 用于指定自定义 OP 对应的源码文件。cpp 源文件支持。cc、.cpp等后缀；cuda 源文件以。cu 为后缀。
  - **\*args, \*\*kwargs** (可选) - 用于指定 Extension 的其他参数，支持的参数与 ``setuptools.Extension`` 一致。

返回
::::::::::::
 ``setuptools.Extension`` 对象。
