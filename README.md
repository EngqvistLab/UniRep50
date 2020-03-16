# Description
UniRep50 model from George Church

Originally cloned from:
https://github.com/churchlab/UniRep

Modified by Martin Engqvist

## Requirements
Assuming that you use Miniconda (https://docs.conda.io/en/latest/miniconda.html) or Anaconda (https://www.anaconda.com/) the required packages can be easily installed from the yml file `packages.yml`. In a terminal execute:
```bash
conda env create -f packages.yml
conda activate tf1
```

## Installation
Download repository and unzip (alternatively fork or clone), cd to the project base folder and execute the command below:

```bash
pip3 install -e .
```

If using an anaconda environment you may have to first locate the miniconda pip using whereis.
```bash
whereis pip
```

Locate the appropriate file path (the one that has anaconda and the correct environment in the filepath) and run the modified command. For example:

```bash
/home/username/miniconda3/envs/py37/bin/pip install -e .
```

The library should now be available for loading in all your python scripts.


## Usage

```python
from unirep.run_inference import BatchInference
inf_obj = BatchInference(batch_size=256)
df = inf_obj.run_inference(filepath='my_sequences.fasta')
df.to_csv('my_sequences_embeddings.tsv', sep='\t')
```


## License
Copyright 2018, 2019 Ethan Alley, Grigory Khimulya, Surojit Biswas

All the model weights are licensed under the terms of Creative Commons Attribution-NonCommercial 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by-nc/4.0/ or send a letter to Creative Commons, PO Box 1866, Mountain View, CA 94042, USA.

Otherwise the code in this repository is licensed under the terms of [GPL v3](https://www.gnu.org/licenses/gpl-3.0.html) as specified by the gpl.txt file.

