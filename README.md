# Attention-embedded Deep Reinforcement Learning for Highway Lane Navigation

See here for the report and short ppt:
- https://drive.google.com/file/d/1-j0cHv-IyCzf1BdYGt1Ni-X1n8gNX_78/view?usp=drive_link
- https://docs.google.com/presentation/d/1-jAHBmUzJaIDbUstOdlDh8LHfU66nDYu/edit?usp=drive_link&ouid=112687757016813129635&rtpof=true&sd=true

### Getting started
Conda environment with python>=3.6 is used during the experiments.
```sh
# Installing the packages (can use pip install -e ./<PACKAGE NAME>)
cd highway-env/
python3 setup.py install
cd ../rl-agents/
python3 setup.py install

pip install torch-scatter torch-sparse torch-cluster torch-spline-conv torch-geometric

```


### Training and Testing
Change directory to `rl-agents/scripts/`. 

To train, run:

```
python experiments.py evaluate configs/HighwayEnv/env.json configs/HighwayEnv/agents/DQNAgent/ego_attention.json --train --episodes=3000 --name-from-config
```

To test, edit the `--recover-from` flag and run:
```
python experiments.py evaluate configs/HighwayEnv/env.json configs/HighwayEnv/agents/DQNAgent/ego_attention.json --test --episodes=10 --name-from-config --recover-from=<PATH TO OUTPUT DIR>
```


TODO: 
- Clean the code
- Update README.md 