page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.math.multiply

### Aliases:

* `tf.RaggedTensor.__mul__`
* `tf.math.multiply`
* `tf.multiply`

``` python
tf.math.multiply(
    x,
    y,
    name=None
)
```



Defined in [`tensorflow/python/ops/math_ops.py`](https://github.com/tensorflow/tensorflow/blob/r1.13/tensorflow/python/ops/math_ops.py).

Returns x * y element-wise.

*NOTE*: `<a href="../../tf/math/multiply"><code>tf.multiply</code></a>` supports broadcasting. More about broadcasting
[here](http://docs.scipy.org/doc/numpy/user/basics.broadcasting.html)

#### Args:

* <b>`x`</b>: A `Tensor`. Must be one of the following types: `bfloat16`, `half`, `float32`, `float64`, `uint8`, `int8`, `uint16`, `int16`, `int32`, `int64`, `complex64`, `complex128`.
* <b>`y`</b>: A `Tensor`. Must have the same type as `x`.
* <b>`name`</b>: A name for the operation (optional).


#### Returns:

A `Tensor`. Has the same type as `x`.