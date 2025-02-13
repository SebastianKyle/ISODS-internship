# ISODS Internship Entrance Test

This repository contains a Jupyter Notebook for fine-tuning a VITS text-to-speech model in Vietnamese using Piper and performing lip syncing using Wav2Lip

I use the video of myself for lip syncing. And since the pretrained VITS model from [piper](https://github.com/rhasspy/piper) use female voice, I have to fine-tune it using a small dataset of audio files from a male speaker. The dataset can be found at [vivos](https://huggingface.co/datasets/AILAB-VNUHCM/vivos) and I use audios from speaker number 33.

## Prerequisites
- Google Colab with GPU support
- Required packages will be listed in the notebook

## Instructions

- The notebook starts off with code cells for fine-tuning a pretrained text-to-speech model (Vietnamese) from [piper](https://github.com/rhasspy/piper) to use a male voice. This process would take time (probably somewhere more than an hour) so one can skip the fine-tuning process by finishing the cells which install the required packages for piper (before the 'Download datasets' markdown cell) and then continue at the code cells after the 'Download fine-tuned model (to skip training phase)' markdown cell.

- The code will download the fine-tuned model in ONNX format and its json config file.

- Then, one can continue to run the cells below the 'Test inference' markdown block to write text file as input and convert the text to speech using piper inference.

- After testing with the fine-tuned text-to-speech model, one can continue to the 'Lip Sync' section which uses [Wav2Lip](https://github.com/Rudrabha/Wav2Lip) library to create lip sync video for provided speech. Please follow the instructions and execute code cells, especially the cell that mentions modifying the code in Wav2Lip library which guide user to modify code in the _build_mel_basis() method so that the inference process of Wav2Lip can run without errors. 

## Additional Information
- The notebook includes detailed comments and instructions for each step.
- Fine-tuned VITS model and reference video will be installed from shared google drive files in the notebook using gdown.
- Feel free to modify any paths or configurations as needed for your environment.

## Contact
For any questions or issues, please contact [me](mailto:doantanqn000@gmail.com).