# Minegrad: Gradient Inversion Attacks on LoRA Fine-Tuning

## 📝 Abstract

Parameter-efficient fine-tuning (PEFT), such as low-rank adaptation (LoRA), has recently been adopted in federated learning to reduce communication and computation costs. In this setup, users download a pretrained model from the server prior to fine-tuning, and then fine-tune lightweight LoRA modules locally while keeping the pretrained model frozen, sharing only the gradients of the fine-tuning parameters with the server. Despite its growing popularity, robustness of federated fine-tuning against an adversarial server remains underexplored, where the server maliciously tampers with the training protocol to breach the privacy of users’ data. In this work, we investigate gradient inversion attacks on LoRA fine-tuning. We propose an analytical attack that enables a malicious server to recover private user data by leveraging a poisoned pretrained model and fine-tuning parameters. Our design embeds fine-tuning data within the shared gradients, to allow the server to analytically reconstruct user data. Unlike prior works, our attack is applicable to both language and vision tasks, does not rely on computationally expensive (adversarial) pretraining with public datasets or require the number of training tokens to be less than the rank of LoRA modules. Experimental results on both language and vision tasks demonstrate high-fidelity data recovery across multiple baselines, revealing several critical vulnerabilities.

<img src="Attack_image.jpg" width="800"/>

This repository contains the code associated with the attack propsed in the paper.

## Short Details about the Files
1. Design_Model_LORA.py contains the malicious design of some layers from pretrained model.
2. roberta_module.py contains the code for inserting LORA modules in the Roberta-base architecture.
3. User_Train.py contains the code for training in the user side.
4. reconstruction.py contains the code for reconstructing fine-tuning sample from the gradients.
5. Run LORA_Attack.ipynb that will call all the functions in the above files and output recovered texts.
6. This is a sample code for training on Yahoo Answers dataset.

## If you find this project useful, please cite
```bibtex
@inproceedings{MineGrad2026,
  title={MineGrad: Gradient Inversion Attacks on LoRA Fine-Tuning},
  author={Sami, Hasin Us and Sen, Swapneel and Guler, Basak},
  booktitle={Proceedings of the Twenty-Ninth Annual Conference on Artificial Intelligence and Statistics (AISTATS)},
  year={2026}
}
```
