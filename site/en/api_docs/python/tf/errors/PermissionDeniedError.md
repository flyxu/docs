page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.errors.PermissionDeniedError

## Class `PermissionDeniedError`

Inherits From: [`OpError`](../../tf/errors/OpError)



Defined in [`tensorflow/python/framework/errors_impl.py`](https://github.com/tensorflow/tensorflow/blob/r1.13/tensorflow/python/framework/errors_impl.py).

Raised when the caller does not have permission to run an operation.

For example, running the
<a href="../../tf/ReaderBase#read"><code>tf.WholeFileReader.read</code></a>
operation could raise `PermissionDeniedError` if it receives the name of a
file for which the user does not have the read file permission.


<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    node_def,
    op,
    message
)
```

Creates a `PermissionDeniedError`.



## Properties

<h3 id="error_code"><code>error_code</code></h3>

The integer error code that describes the error.

<h3 id="message"><code>message</code></h3>

The error message that describes the error.

<h3 id="node_def"><code>node_def</code></h3>

The `NodeDef` proto representing the op that failed.

<h3 id="op"><code>op</code></h3>

The operation that failed, if known.

*N.B.* If the failed op was synthesized at runtime, e.g. a `Send`
or `Recv` op, there will be no corresponding
<a href="../../tf/Operation"><code>tf.Operation</code></a>
object.  In that case, this will return `None`, and you should
instead use the <a href="../../tf/errors/OpError#node_def"><code>tf.errors.OpError.node_def</code></a> to
discover information about the op.

#### Returns:

The `Operation` that failed, or None.


