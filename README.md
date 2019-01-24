# NATTACK: A STRONG AND UNIVERSAL GAUSSIAN BLACK-BOX ADVERSARIAL ATTACK


Data and model can be found here: [data and model](https://1drv.ms/f/s!AlXveXe2-CcAhc9mY5XOfDMJjZIiVQ).
 

Please download the data&&model and unzip them to './cifar-data' and './all_models'
 
 
Below is Table 1 from our paper, where we show the robustness of each accepted defense to the adversarial examples we can construct:



| Defense | Dataset | Distance | Success rate |
|---|---|---|---|
| ADV-TRAIN [Madry et al. (2018)](https://arxiv.org/abs/1706.06083) | CIFAR | 0.031 (linf) | 47.9% |
| ADV-BNN [Liu et al. (2019)](https://arxiv.org/abs/1810.01279) | CIFAR | 0.031 (linf) | 75.3% |
| THERM-ADV Buckman et al. (2018)[Madry et al. (2018)](https://arxiv.org/abs/1706.06083) | CIFAR | 0.031 (linf) | 91.2% |
| CAS-ADV [Na et al. (2018)](https://arxiv.org/abs/1708.02582) | CIFAR | 0.015 (linf) | 97.7% |
| ADV-GAN [Wang & Yu (2019)](https://openreview.net/forum?id=S1lIMn05F7) | CIFAR | 0.015 (linf) | 97.7% |
| LID [Ma et al. (2018)](https://arxiv.org/abs/1801.02613) | CIFAR | 0.031 (linf) | 100.0% |
| THERM [Buckman et al. (2018)](https://openreview.net/forum?id=S18Su--CW) | CIFAR | 0.031 (linf) | 100.0% |
| SAP [Dhillon et al. (2018)](https://arxiv.org/abs/1803.01442) | CIFAR | 0.031 (linf) | 100.0% |
| RSE [Liu et al. (2018)](https://arxiv.org/abs/1712.00673) | CIFAR | 0.031 (linf) | 100.0% |
| GUIDED DENOISER [(Liao et al., 2018)](https://arxiv.org/abs/1711.00117) | ImageNet | 0.031 (linf) | 95.5% |
| RANDOMIZATION [Xie et al. (2018)](https://arxiv.org/abs/1711.01991) | ImageNet | 0.031 (linf) | 96.5% |
| INPUT-TRANS [Guo et al. (2018)](https://arxiv.org/abs/1711.00117) | ImageNet | 0.005 (l2) | 100.0% |
| PIXEL DEFLECTION [Prakash et al. (2018)](https://arxiv.org/abs/1801.08926) | ImageNet | 0.031 (linf) | 100.0% |




## Paper

**Abstract:**

Powerful adversarial attack methods are vital for understanding how to construct robust deep neural networks (DNNs) and for thoroughly testing defense techniques. In this paper, we propose a black-box adversarial attack algorithm that can defeat both vanilla DNNs and those generated by various defense techniques developed recently. Instead of searching for an "optimal" adversarial example for a benign input to a targeted DNN, our algorithm finds a probability density distribution over a small region centered around the input, such that a sample drawn from this  distribution is likely an adversarial example, without the need of accessing the DNN's internal layers or weights. Our approach is universal as it can successfully attack different neural networks by a single algorithm. It is also strong; according to the testing against 2 vanilla DNNs and 13 defended ones, it outperforms state-of-the-art black-box or white-box attack methods for most test cases. Additionally, our results reveal that adversarial training remains one of the best defense techniques, and the adversarial examples are not as transferable across defended DNNs as them across vanilla DNNs. 


## Source code

This repository contains our implemenation of the black-box attack algorithm described in our paper, six defense methods (SAP, LID, RANDOMIZATION, INPUT-TRANS, THERM, and THERM-DAV) borrowed from the code of Anish et al. (2018), two defended models (GUIDED DENOISER and PIXEL DEFLECTION) based on the code of Athalye & Carlini, (2018), and two defended models (RSE and CAS-ADV) from the original papers.

## Note

Please note the paper is still under double-blind review.
