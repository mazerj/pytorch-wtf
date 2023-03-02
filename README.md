# pytorch-wtf


## When is 1 != 1?
```python
$ python 
Python 3.8.10 (default, Nov 14 2022, 12:59:47) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import torch
>>> torch.__version__
'1.10.2+cu113'
>>> assert 111/torch.Tensor([111]) == 1
>>> assert torch.Tensor([110])/torch.Tensor([110]) == 1
>>> assert 110/torch.Tensor([110]) == 1
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AssertionError
>>> ```
