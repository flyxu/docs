page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.compat.v2.reduce_mean


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/ops/math_ops.py#L1815-L1870">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Computes the mean of elements across dimensions of a tensor.

### Aliases:

* <a href="/api_docs/python/tf/compat/v2/reduce_mean"><code>tf.compat.v2.math.reduce_mean</code></a>


``` python
tf.compat.v2.reduce_mean(
    input_tensor,
    axis=None,
    keepdims=False,
    name=None
)
```



<!-- Placeholder for "Used in" -->

Reduces `input_tensor` along the dimensions given in `axis`.
Unless `keepdims` is true, the rank of the tensor is reduced by 1 for each
entry in `axis`. If `keepdims` is true, the reduced dimensions
are retained with length 1.

If `axis` is None, all dimensions are reduced, and a
tensor with a single element is returned.

#### For example:



```python
x = tf.constant([[1., 1.], [2., 2.]])
tf.reduce_mean(x)  # 1.5
tf.reduce_mean(x, 0)  # [1.5, 1.5]
tf.reduce_mean(x, 1)  # [1.,  2.]
```

#### Args:


* <b>`input_tensor`</b>: The tensor to reduce. Should have numeric type.
* <b>`axis`</b>: The dimensions to reduce. If `None` (the default), reduces all
  dimensions. Must be in the range `[-rank(input_tensor),
  rank(input_tensor))`.
* <b>`keepdims`</b>: If true, retains reduced dimensions with length 1.
* <b>`name`</b>: A name for the operation (optional).


#### Returns:

The reduced tensor.




#### Numpy Compatibility
Equivalent to np.mean

Please note that `np.mean` has a `dtype` parameter that could be used to
specify the output type. By default this is `dtype=float64`. On the other
hand, <a href="../../../tf/math/reduce_mean"><code>tf.reduce_mean</code></a> has an aggressive type inference from `input_tensor`,
for example:

```python
x = tf.constant([1, 0, 1, 0])
tf.reduce_mean(x)  # 0
y = tf.constant([1., 0., 1., 0.])
tf.reduce_mean(y)  # 0.5
```