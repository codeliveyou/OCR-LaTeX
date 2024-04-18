# LaTeX OCR

The goal of this project is to create a learning based system that takes an image of a math formula and returns corresponding LaTeX code. 

![header](https://user-images.githubusercontent.com/55287601/109183599-69431f00-778e-11eb-9809-d42b9451e018.png)

## Using the model
To run the model you need Python 3.7+

If you don't have PyTorch installed. Follow their instructions [here](https://pytorch.org/get-started/locally/).

Install the package `pix2tex`: 

```
pip install "pix2tex[gui]"
```

![demo](https://user-images.githubusercontent.com/55287601/117812740-77b7b780-b262-11eb-81f6-fc19766ae2ae.gif)

If the model is unsure about the what's in the image it might output a different prediction every time you click "Retry". With the `temperature` parameter you can control this behavior (low temperature will produce the same result).

## Model
The model consist of a ViT [[1](#References)] encoder with a ResNet backbone and a Transformer [[2](#References)] decoder.

### Performance
| BLEU score | normed edit distance | token accuracy |
| ---------- | -------------------- | -------------- |
| 0.88       | 0.10                 | 0.60           |
