Release notes
=============

0.4.0
-----
Tonic is now free from direct PyTorch and PyTorch Vision dependencies, meaning that if someone wanted to use it with another pipeline (e.g. TensorFlow), they would be able to do so. This release is the first step to making Tonic more flexible in that respect. For previous users that mainly means that ``tonic.datasets.DataLoader`` is no longer available anymore, which had been an alias for the pytorch dataloader. Now you will have to import the class directly like so:
::

  import torch
  dataloader = torch.utils.data.DataLoader(dataset)
