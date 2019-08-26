# BvhToMimic 

## Installation
`pip install bvhtodeepmimic`    
or  
`pip3 install bvhtodeepmimic`

Will install the library together with the requirements. Currently works with python 3.6 or 3.7

## Usage
Create a BvhConverter object:
```python
from bvhtomimic import BvhConverter
converter = BvhConverter("./Settings/settings.json")
```

Generate the DeepMimic text from a .bvh file:
```python
converter.convertBvhFile("pathToBvhFile", loop=False)
```

Or write directly to file:
```python
converter.writeDeepMimicFile(pathToBvhFile, outputPath)
```

Or use [the example script](./example_script.py) that will convert all .bvh files located in ./InputBvh/ into Mimic Motion files, located in ./OutputMimic/ .

## Creating a settings file

Currently joints in .bvh files have to be manually assigned by name to the corresponding joints in the DeepMimic humanoid model. This is done by assigning the .bvh model's bone names to the corresponding joint properties in [./Settings/settings.json](./Settings/settings.json). On top of the joint assignments, this file should also include settings to change the scale by which the .bvh file should be transformed, and the joints used to identify the **root** rotation of the model.

## Related Projects

[List of related projects](https://github.com/SleepingFox88/DeepMimic-Animation-Conversion)
