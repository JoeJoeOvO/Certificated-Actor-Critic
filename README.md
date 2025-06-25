# [ICRA2025] Certificated Actor-Critic: Hierarchical Reinforcement Learning with Control Barrier Functions for Safe Navigation

<!-- **HardNet** is a framework for constructing neural networks that inherently satisfy hard constraints without sacrificing model capacity.
By appending a differentiable enforcement layer to the network's output, HardNet ensures that the outputs adhere to specified input-dependent constraints, enabling unconstrained optimization of network parameters using standard algorithms. -->

This repository reproduces the algorithm called **Certificated Actor-Critic (CAC)** in our paper "[Certificated Actor-Critic: Hierarchical Reinforcement Learning with Control Barrier Functions for Safe Navigation](https://arxiv.org/pdf/2501.17424)."

If you use this work in your research, please cite:
```bibtex
@article{xie2025certificated,
  title={Certificated Actor-Critic: Hierarchical Reinforcement Learning with Control Barrier Functions for Safe Navigation},
  author={Xie, Junjun and Zhao, Shuhao and Hu, Liang and Gao, Huijun},
  journal={arXiv preprint arXiv:2501.17424},
  year={2025}
}

```
<!-- 
## 📁 Repository Structure

- `hardnet_aff.py`: HardNet-Aff implementation for input-dependent affine constraints
- `hardnet_cvx.py`: HardNet-Cvx implementation for input-dependent convex constraints
- `baseline_dc3.py`, `baseline_nn.py`, `baseline_opt.py`, `baseline_cbfqp.py`: Baseline models for comparison
- `exp_cbf.ipynb`, `exp_gradient.ipynb`, `exp_opt.ipynb`, `exp_pwc.ipynb` `exp_pwcbox.ipynb`: Notebooks demonstrating experiments and use cases
- `datasets/`: Datasets used in experiments
- `utils.py`: Utility functions
- `test_nets.py`: Evaluation for comparison
- `requirements.txt`: Python dependencies
- `run_expers.sh`: Shell script to run experiments

## 🚀 Usage

For example, to use HardNet-Aff for the experiment of learning with piecewise constraints,
```python
python hardnet_aff.py --probType pwc
```
To train multiple models via different methods, run a bash script with
```bash
for i in 1 2 3 4 5
do
    for probType in pwc
    do
        python baseline_dc3.py --probType $probType  --seed $i
        python baseline_nn.py --probType $probType  --seed $i
        python baseline_nn.py --probType $probType --suffix _noSoft --softWeight 0.0 --seed $i
        python hardnet_aff.py --probType $probType --seed $i
    done
done
```
To generate evaluation statistics,
```python
python test_nets.py --probType toy --expDir results/PWCProblem-50
```
Run the Jupyter notebook `exp_pwc.ipynb` for visualization and getting tables -->