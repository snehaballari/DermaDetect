
# DermaDetect
An AI-based tool for preliminary diagnosis of dermatological conditions using image processing.

## Features  
DermaDetect provides instant, browser-based inference on uploaded lesion images using a fine-tuned MobileNet V2 backbone in PyTorch  ([MobileNet v2 - PyTorch](https://pytorch.org/hub/pytorch_vision_mobilenet_v2/)).  
It distinguishes five clinically relevant classes—Actinic Keratosis, Alopecia, Chondrodermatitis Nodularis, Keloids, and Molluscum Contagiosum—trained on the DermNet Dataset.
The custom Gradio Blocks UI automatically triggers inference on upload, displays just the single input image, and presents both the top prediction and a full probability table without redundant previews  ([Image Classification in TensorFlow and Keras - Gradio](https://www.gradio.app/guides/image-classification-in-tensorflow)).  
All dependencies are cached for rapid startup, and the app can be shared publicly with a single parameter toggle.  

## Installation  
```bash
pip install torch torchvision gradio pillow pandas
```  

## Usage  
1. Place your fine-tuned `c5mobnetv2.pth` in the `/content/` folder.  
2. Run the provided Colab/Local notebook cell; the Gradio interface will launch automatically.  
3. Upload any lesion image (JPG/PNG) to see the single-image display, predicted class, and probability distribution table.  

## Model Architecture  
We leverage the **MobileNet V2** inverted residual and linear bottleneck design for lightweight, accurate feature extraction on dermoscopic images.  

## Dataset  
Training uses the **[DermNet](https://www.dermnetnz.org/image-library/)** dataset, a large multi-source collection widely adopted in skin disease classification tasks.  

## License  
MIT License - see [LICENSE](LICENSE).  
```


