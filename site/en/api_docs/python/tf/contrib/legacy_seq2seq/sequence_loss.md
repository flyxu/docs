page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.legacy_seq2seq.sequence_loss


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/contrib/legacy_seq2seq/python/ops/seq2seq.py#L1103-L1143">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Weighted cross-entropy loss for a sequence of logits, batch-collapsed.

``` python
tf.contrib.legacy_seq2seq.sequence_loss(
    logits,
    targets,
    weights,
    average_across_timesteps=True,
    average_across_batch=True,
    softmax_loss_function=None,
    name=None
)
```



<!-- Placeholder for "Used in" -->


#### Args:


* <b>`logits`</b>: List of 2D Tensors of shape [batch_size x num_decoder_symbols].
* <b>`targets`</b>: List of 1D batch-sized int32 Tensors of the same length as logits.
* <b>`weights`</b>: List of 1D batch-sized float-Tensors of the same length as logits.
* <b>`average_across_timesteps`</b>: If set, divide the returned cost by the total
  label weight.
* <b>`average_across_batch`</b>: If set, divide the returned cost by the batch size.
* <b>`softmax_loss_function`</b>: Function (labels, logits) -> loss-batch to be used
  instead of the standard softmax (the default if this is None). **Note that
  to avoid confusion, it is required for the function to accept named
  arguments.**
* <b>`name`</b>: Optional name for this operation, defaults to "sequence_loss".


#### Returns:

A scalar float Tensor: The average log-perplexity per symbol (weighted).



#### Raises:


* <b>`ValueError`</b>: If len(logits) is different from len(targets) or len(weights).