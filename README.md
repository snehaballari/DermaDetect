# DermaDetect
An AI-based tool for preliminary diagnosis of dermatological conditions using image processing.

This README introduces **DermaDetect**, a PyTorch-based skin lesion classification tool served through a streamlined Gradio interface. Below you’ll find detailed sections on features, installation, usage, architecture, data, performance, and contribution guidelines—organized per GitHub best practices to get you up and running quickly.

## Features  
DermaDetect provides instant, browser-based inference on uploaded lesion images using a fine-tuned MobileNet V2 backbone in PyTorch  ([MobileNet v2 - PyTorch](https://pytorch.org/hub/pytorch_vision_mobilenet_v2/?utm_source=chatgpt.com)).  
It distinguishes five clinically relevant classes—Actinic Keratosis, Alopecia, Chondrodermatitis Nodularis, Keloids, and Molluscum Contagiosum—trained on the DermNet Dataset.
The custom Gradio Blocks UI automatically triggers inference on upload, displays just the single input image, and presents both the top prediction and a full probability table without redundant previews  ([Image Classification in TensorFlow and Keras - Gradio](https://www.gradio.app/guides/image-classification-in-tensorflow?utm_source=chatgpt.com), [Image Classification In Pytorch - Gradio](https://www.gradio.app/guides/image-classification-in-pytorch?utm_source=chatgpt.com)).  
All dependencies are cached for rapid startup, and the app can be shared publicly with a single parameter toggle  ([Image Classification in TensorFlow and Keras - Gradio](https://www.gradio.app/guides/image-classification-in-tensorflow?utm_source=chatgpt.com)).  


## Installation  
Clone this repository and install dependencies with:
```bash
pip install torch torchvision gradio pillow pandas
```  
This minimal set ensures you have PyTorch, the MobileNet V2 model, Gradio for the UI, and data handling libraries  ([MobileNet V2 — Torchvision main documentation - PyTorch](https://pytorch.org/vision/main/models/mobilenetv2.html?utm_source=chatgpt.com)).  

## Usage  
1. Place your fine-tuned `c5mobnetv2.pth` in the `/content/` folder.  
2. Run the provided Colab/Local notebook cell; the Gradio interface will launch automatically.  
3. Upload any lesion image (JPG/PNG) to see the single-image display, predicted class, and probability distribution table  ([Image Classification In Pytorch - Gradio](https://www.gradio.app/guides/image-classification-in-pytorch?utm_source=chatgpt.com)).  

## Model Architecture  
We leverage the **MobileNet V2** inverted residual and linear bottleneck design for lightweight, accurate feature extraction on dermoscopic images  ([MobileNet v2 - PyTorch](https://pytorch.org/hub/pytorch_vision_mobilenet_v2/?utm_source=chatgpt.com)).  

## Dataset  
Training uses the **DermNet**  dataset, a large multi-source collection widely adopted skin disease classification tasks.   

## License  
This project is released under the MIT License—see [LICENSE](LICENSE) for details.  

