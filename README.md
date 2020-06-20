# CIFAR100 Coarse
Simple function that converts CIFAR100 in PyTorch from sparse labels to coarse labels based on superclass. 

### Usage 1: Update using function `sparse2coarse`
```
trainset = torchvision.datasets.CIFAR100(root)
trainset.targets = sparse2coarse(trainset.targets)    # update labels 
```

### Usage 2: Import new dataset class `CIFAR100Coarse`
Class defined in [`cifar100coarse.py`](./cifar100coarse.py).

```
from cifar100coarse import CIFAR100Coarse

trainset = CIFAR100Coarse(root, train=True, transform=None, target_transform=None, download=False)
```

### Superclasses
```
superclass = [['beaver', 'dolphin', 'otter', 'seal', 'whale'],
              ['aquarium_fish', 'flatfish', 'ray', 'shark', 'trout'],
              ['orchid', 'poppy', 'rose', 'sunflower', 'tulip'],
              ['bottle', 'bowl', 'can', 'cup', 'plate'],
              ['apple', 'mushroom', 'orange', 'pear', 'sweet_pepper'],
              ['clock', 'keyboard', 'lamp', 'telephone', 'television'],
              ['bed', 'chair', 'couch', 'table', 'wardrobe'],
              ['bee', 'beetle', 'butterfly', 'caterpillar', 'cockroach'],
              ['bear', 'leopard', 'lion', 'tiger', 'wolf'],
              ['bridge', 'castle', 'house', 'road', 'skyscraper'],
              ['cloud', 'forest', 'mountain', 'plain', 'sea'],
              ['camel', 'cattle', 'chimpanzee', 'elephant', 'kangaroo'],
              ['fox', 'porcupine', 'possum', 'raccoon', 'skunk'],
              ['crab', 'lobster', 'snail', 'spider', 'worm'],
              ['baby', 'boy', 'girl', 'man', 'woman'],
              ['crocodile', 'dinosaur', 'lizard', 'snake', 'turtle'],
              ['hamster', 'mouse', 'rabbit', 'shrew', 'squirrel'],
              ['maple_tree', 'oak_tree', 'palm_tree', 'pine_tree', 'willow_tree'],
              ['bicycle', 'bus', 'motorcycle', 'pickup_truck', 'train'],
              ['lawn_mower', 'rocket', 'streetcar', 'tank', 'tractor']]
```


### Reference
CIFAR10/100 website: `https://www.cs.toronto.edu/~kriz/cifar.html` 
