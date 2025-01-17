
# **Playing trading games with deep reinforcement learning**
## Structure
```
.
|-- .gitignore
|-- LICENSE
|-- README.md
|-- data
|   |-- PairSamplerDB
|   |   |-- randjump_100,1(10,\ 30)[]_A
|   |   |   |-- db.pickle
|   |   |   `-- param.json
|   |   `-- randjump_100,1(10,\ 30)[]_B
|   |       |-- db.pickle
|   |       `-- param.json
|   `-- SinSamplerDB
|       |-- concat_half_base_A
|       |   |-- db.pickle
|       |   `-- param.json
|       `-- concat_half_base_B
|           |-- db.pickle
|           `-- param.json
|-- env.yml
|-- paper.pdf
`-- src
    |-- agents.py
    |-- emulator.py
    |-- lib.py
    |-- main.py
    |-- sampler.py
    |-- simulators.py
    `-- visualizer.py

```


This repo is the code for this [paper](https://arxiv.org/abs/1803.03916). Deep reinforcement learing is used to find optimal strategies in these two scenarios:
* Momentum trading: capture the underlying dynamics
* Arbitrage trading: utilize the hidden relation among the inputs

Several neural networks are compared: 
* Recurrent Neural Networks (GRU/LSTM)
* Convolutional Neural Network (CNN)
* Multi-Layer Perception (MLP)

### Dependencies

You can get all dependencies via the [Anaconda](https://conda.io/docs/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file) environment file, [env.yml](https://github.com/golsun/deep-RL-time-series/blob/master/env.yml):
```
    # conda env create -f env.yml
    conda env create -f env2.yml
```
### Play with it
Just call the main function
```
    python main.py
```
You can play with model parameters (specified in main.py), if you get good results or any trouble, please contact me at gxiang1228@gmail.com
