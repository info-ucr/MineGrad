# Minegrad: Gradient Inversion Attacks on LoRA Fine-Tuning
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
```bibtex
