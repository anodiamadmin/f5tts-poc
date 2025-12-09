---
license: apache-2.0
language:
- en
pipeline_tag: text-to-speech
tags:
- voice cloning
library_name: f5-tts
---

# OpenF5 TTS Base (Alpha)

OpenF5 TTS is an open-weight text-to-speech model with support for zero-shot voice cloning based on and trained with the [F5-TTS](https://github.com/SWivid/F5-TTS) framework.

The main difference from the original F5-TTS model is the license of the model. Due to the training data, the F5-TTS model was licensed under a non-commercial license (CC BY-NC). This model was trained on permissively licensed data and is **available under the Apache 2.0 license**, which means it can be used for **both commercial and personal purposes**.

> [!TIP]
> This model is **still in alpha.** Performance and stability may suffer. The main goal for this model is to create a permissively-licensed base for further fine-tuning. However, the current model is still inferior to the official NC-licensed F5-TTS model.
> 
> New variants will soon be released with more post-training/fine-tuning. These version will have:
> 
> 1. Better voice cloning capabilities with increased speaker similarity
> 2. Enhanced emotional speech generation
> 3. More stable performance
>
> The current model is only a base model, much more is coming soon - stay tuned!

## Details

This model was trained using the F5-TTS Base V1 model configuration for 1 million steps on the Emilia-YODAS dataset. The model was only trained on English speech.

## Usage

```
pip install f5-tts
huggingface-cli download mrfakename/OpenF5-TTS --local-dir openf5
f5-tts_infer-cli -mc openf5/config.yaml -p openf5/model.pt -v openf5/vocab.txt
```

## Safety

This model is provided under the Apache 2.0 License. Users are encouraged to consider the ethical and societal impacts of synthetic speech technologies. Potential misuse - including impersonation, deception, or violation of privacy - can lead to harm. While the license permits broad usage, responsible application is advised, particularly in contexts involving identifiable individuals or public communication. This model is intended to support research, accessibility, and creative work in a transparent and accountable manner.

## Acknowledgements

Special thanks to [Hugging Face](https://huggingface.co/) for providing the compute to train this model.

Thanks to the authors of [F5-TTS](https://github.com/SWivid/F5-TTS) for releasing the great F5-TTS model and codebase and lucidrains for the original open-source [E2-TTS implementation](https://github.com/lucidrains/e2-tts-pytorch).

Additionaly, thanks to Amphion for the wonderful [Emilia-YODAS dataset](https://huggingface.co/datasets/amphion/Emilia-Dataset) - without it, this project wouldn't have been possible.

## License

This model is licensed under the Apache 2.0 license. You are free to use it for both **commercial** and **non-commercial** purposes.