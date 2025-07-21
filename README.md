
Neural Style Transfer using TensorFlow Hub

This project implements **Neural Style Transfer** using TensorFlow and TensorFlow Hub. It takes a content image and a style image, and produces a new image that looks like the content image "painted" in the style of the second image.

Model Used

* **Arbitrary Image Stylization** model from TensorFlow Hub:
  [`https://tfhub.dev/google/magenta/arbitrary-image-stylization-v1-256/2`](https://tfhub.dev/google/magenta/arbitrary-image-stylization-v1-256/2)

Project Structure

```bash
.
├── profile2.jpg              # Content image
├── monet.png                 # Style image
├── generated_img.jpg         # Output image (generated result)
├── style_transfer.py         # Python script with the code
└── README.md                 # Project documentation
```

Dependencies

Install the required libraries using:

```bash
pip install tensorflow tensorflow_hub matplotlib opencv-python
```

How to Run

1. Add your own **content image** (e.g., `profile2.jpg`) and **style image** (e.g., `monet.png`) in the project folder.
2. Run the `style_transfer.py` script.
3. The generated stylized image will be saved as `generated_img.jpg`.

Key Code Highlights

* **Image Preprocessing** is done using TensorFlow.
* **Model Inference** is performed via TF Hub.
* **Stylized Output** is visualized using `matplotlib` and saved using `OpenCV`.

```python
stylized_image = model(tf.constant(content_image), tf.constant(style_image))[0]
```

Output Example

The output image combines:

* The structure/content of the content image (`profile2.jpg`)
* The artistic style of the style image (`monet.png`)

