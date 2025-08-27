# Blob Localization

This project trains a CNN model to detect and localize blobs in grayscale images.

## Workflow

1. **Data**

   * Images generated with random blobs
   * Labels: binary masks of blob locations (provided while creating the blob)

2. **Model**

   * Uses VGG16 + Dense Layer,GlobalAvgPooling

3. **Usage**

   ```python
   pred = model.predict(x)
   ```

   * `x`: batch of images
   * `pred`: predicted masks

## Notes

* Batch size: 64
* Predictions are grayscale masks
* Works on synthetic blob dataset
* Working on Cat Dataset too.
