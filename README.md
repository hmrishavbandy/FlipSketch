
<div align="center" id = "user-content-toc">
<img align="left" width="70" height="70" src="https://github.com/user-attachments/assets/c61cec76-3c4b-42eb-8c65-f07e0166b7d8" alt="">
  
  # [FlipSketch: Flipping Static Drawings to Text-Guided Sketch Animations [CVPR 2025] ](https://hmrishavbandy.github.io/flipsketch-web/)
  [![arXiv](https://img.shields.io/badge/arXiv-2411.10818-b31b1b.svg)]([https://arxiv.org/abs/1234.56789](https://arxiv.org/abs/2411.10818)) [![Open in Spaces](https://huggingface.co/datasets/huggingface/badges/resolve/main/open-in-hf-spaces-md.svg)](https://huggingface.co/spaces/Hmrishav/FlipSketch)
 <br>
[Hmrishav Bandyopadhyay](https://hmrishavbandy.github.io/) . [Yi-Zhe Song](https://personalpages.surrey.ac.uk/y.song/)
</div>


https://github.com/user-attachments/assets/de8f2cef-3123-4a98-90e0-af59631a00f4

<div align="center"> 

## ✨ Sketch + Text &#8594; Animation ✨

![flipsketch_main](https://github.com/user-attachments/assets/e20405bb-2958-484d-9c13-042bac8b40d5)

</div>
<div align="center"> 
  
## 🎥 Gallery 🎥
<div  style="display: flex; flex-wrap: wrap; justify-content: center; gap: 15px; padding: 10px;">
  <img src="https://github.com/user-attachments/assets/27ece2d1-f3fa-40fe-82a6-87681ec19443" alt="gazelle" style="width: 150px; height: 150px; object-fit: cover;">
  <img src="https://github.com/user-attachments/assets/fecbc5f5-c4ac-48b4-91b0-655e4e259c03" alt="cat" style="width: 150px; height: 150px; object-fit: cover;">
  <img src="https://github.com/user-attachments/assets/e4104224-3dee-49ef-83de-d3ce84e370ba" alt="frame_extrapolation" style="width: 150px; height: 150px; object-fit: cover;">
  <img src="https://github.com/user-attachments/assets/acfc11ae-dc3d-4254-91b9-3d6b220e65fd" alt="fish_base" style="width: 150px; height: 150px; object-fit: cover;">
  <img src="https://github.com/user-attachments/assets/5d8c32cf-e2fe-4704-a860-a855afb45b84" alt="candle" style="width: 150px; height: 150px; object-fit: cover;">
  <img src="https://github.com/user-attachments/assets/ca848252-d0c7-4936-8a2c-9f4c4e7ed05b" alt="surfer-0" style="width: 150px; height: 150px; object-fit: cover;">
  <img src="https://github.com/user-attachments/assets/2d72be9b-596d-4a73-b968-07872ad81dea" alt="flower_v2" style="width: 150px; height: 150px; object-fit: cover;">
  <img src="https://github.com/user-attachments/assets/2d218832-f084-4fe1-8eae-b9696df38c10" alt="horse-2" style="width: 150px; height: 150px; object-fit: cover;">
  <img src="https://github.com/user-attachments/assets/3a97477e-6dcd-4b32-8f6e-cb822afbaebf" alt="squirrel" style="width: 150px; height: 150px; object-fit: cover;">
  <img src="https://github.com/user-attachments/assets/90352cce-1cf6-4403-ae2a-0ddcd08c1fca" alt="pixar_i" style="width: 230px; height: 150px; object-fit: cover;">
</div>
</div>

## 🤗 HuggingFace Demo
Try out our [Hugging Face Space](https://huggingface.co/spaces/Hmrishav/FlipSketch)!

_Powered by ZeroGPU - Special thanks to Hugging Face_ 🙌


## 🚀 QuickStart
- Install conda environment: 
```
conda env create -f flipsketch.yml
```
- Download T2V LoRA Model from HuggingFace
```
git lfs install
git clone https://huggingface.co/Hmrishav/t2v_sketch-lora
```
- Place LoRA checkpoint under root folder:
```
mv t2v_sketch-lora/checkpoint-2500 ./checkpoint-2500/
```
- Run app
```
python app.py
```

## ⚡ PyTorch 2+ Support: 
To use the codebase with PyTorch2.0, modify [here](https://github.com/hmrishavbandy/FlipSketch/blob/7a991e5c657c6da20eba21c13867c5d10324b22f/app.py#L26) to import from `text2vid_torch2.py` instead of `text2vid_modded.py`

## 💡 How it works?

<div align="center">
<img src="./assets/images/model_1.png" alt="Generation Pipeline" width="75%">
<p>We use a T2V model fine-tuned on sketch animations, and condition it to follow an input sketch.</p>
<img src="./assets/images/model_2.png" alt="Noise Refinement" width="75%">
<p>We perform attention composition with reference noise from the input sketch.</p>
</div>

## 🙏🏻 Acknowledgements
- [Live-Sketch](https://github.com/yael-vinker/live_sketch)
- [Text-To-Video-Finetuning](https://github.com/ExponentialML/Text-To-Video-Finetuning)
- [Prompt-To-Prompt](https://github.com/google/prompt-to-prompt)
## 📒 Citation
If you find **FlipSketch** useful, consider citing our work: 

```bibtex
@misc{bandyopadhyay2024flipsketch,
  title={FlipSketch: Flipping static Drawings to Text-Guided Sketch Animations}, 
  author={Hmrishav Bandyopadhyay and Yi-Zhe Song},
  year={2024},
  eprint={2411.10818},
  archivePrefix={arXiv},
  primaryClass={cs.GR},
  url={https://arxiv.org/abs/2411.10818}, 
}
