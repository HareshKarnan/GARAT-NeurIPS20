# An Imitation from Observation Approach to Transfer Learning with Dynamics Mismatch
<img src="images/image36.gif" align="right" width="45%"/>

This repository contains the code for the paper [An Imitation from Observation Approach to Transfer Learning with Dynamics Mismatch](https://proceedings.neurips.cc//paper_files/paper/2020/hash/28f248e9279ac845995c4e9f8af35c2b-Abstract.html), published in Neural Information Processing Systems (NeurIPS) 2020.

### Pre-Requisites

We use `Python3.6`.

The other requirements can be installed using the `requirements.txt` file as follows:

```
python3.6 -m pip install -r requirements.txt
```

We recommend using an [Anaconda](https://www.anaconda.com/) environment, or a [pipenv](https://pypi.org/project/pipenv/) in order to isolate this setup from the rest of your system and causing unintended effects.

### Files
Below we give a description of the file structure.

**data/models/**: store trained *TRPO* agent policies here \
**rl_gat/gat.py**: implements some training utils \
**rl_gat/reinforced_gat.py**: implements *GARAT* \
**test.py**: runs the training routine \
**scripts/run_experiments.sh**: training scripts
**data/models/rarl**: trained RARL (baseline) policies


to launch GARAT on `InvertedPendulum`, run the following :: 

```
bash scripts/run_experiments.sh
```

This script launches one Sim-to-Real experiment on the *InvertedPendulum* domain with the hyperparameters mentioned in the paper.
The above script can be modified to run experiments in the other domains specified in the paper.
Additional hyperparameters can be found in `data/target_policy_params.yaml` and `test.py`.
The modified environment definitions can be found under rl_gat/envs/

### Training the initial policy 

the script can be found in `scripts/train_initial_policy.py` . Modify the name of the environment in ENV_NAME variable. 


