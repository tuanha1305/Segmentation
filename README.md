# Custom High-Accuracy Image Segmentation

This project is a custom implementation inspired by the Dichotomous Image Segmentation (DIS) approach, with modifications to the model and training process.

## Project Structure
```markdown
.
├── data_loader.py
├── dataset_generator.py
├── dataloader_test.py
├── export.py
├── inference.py
├── model/
│   ├── init.py
│   ├── isnet.py
│   ├── modnet.py
│   └── u2net.py
├── requirements.txt
└── train.py
```
## Installation

1. Clone this repository:
   ```bash
    git clone https://github.com/tuanha1305/Segmentation.git
    cd custom-segmentation
   ```
2. Install the required packages:
    ```bash
   pip install -r requirements.txt
   ```

## Dataset

This project uses a custom dataset. The `dataset_generator.py` file contains a `DatasetGenerator` class that creates synthetic data for training and testing. To use your own dataset, modify the `data_loader.py` file accordingly.

## Training

To train the model, run:
```bash
python train.py --net [model_name] --data-dir [path/to/data] --batch-size-train [batch_size] --epoch [num_epochs]
```
Available models: isnet, modnet, u2net

For more training options, please refer to the arguments in `train.py`.

## Testing Data Loader

To test the data loader and visualize the dataset:
```bash
python dataloader_test.py
```

## Inference

To run inference on test images:
```bash
python inference.py --net [model_name] --ckpt [path/to/checkpoint] --data [path/to/test/images] --out [path/to/output]
```

## Model Export

To export the trained model to ONNX format:
```bash
python export.py --net [model_name] --ckpt [path/to/checkpoint] --out [path/to/output.onnx]
```

## Custom Model Architecture

This project includes custom implementations of `ISNet`, `MODNet`, and `U2Net`. The model architectures can be found in the `model/` directory. You can modify these files to experiment with different network structures.

## Evaluation Metrics

The project uses various evaluation metrics including F-measure, Mean Absolute Error (MAE), and structural similarity measures. Refer to the `inference.py` file for implementation details.

## License

The project is licensed under the terms of the [LICENSE](./LICENSE) file.

## Acknowledgements

This project is inspired by the `Dichotomous Image Segmentation (DIS)` approach. We have made significant modifications to suit our specific needs.

## Contact

For any questions or concerns, please open an issue or contact [tuanictu97@gmail.com].