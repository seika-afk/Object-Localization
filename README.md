# Blob Localization

This project trains a CNN model to detect and localize blobs in grayscale images.

## Workflow

1. **Data**

   * Images generated with random blobs
   * Labels: binary masks of blob locations

2. **Model**

   * Simple encoder-decoder CNN
   * Uses Conv2D + MaxPooling for encoding
   * Conv2DTranspose for decoding

3. **Training**

   * Loss: Binary Cross-Entropy
   * Optimizer: Adam
   * Metric: Accuracy

4. **Usage**

   ```python
   pred = model.predict(x)
   ```

   * `x`: batch of images
   * `pred`: predicted masks

5. **Visualization**

   ```python
   plt.imshow(x[0].squeeze(), cmap='gray')       # input image
   plt.imshow(pred[0].squeeze(), cmap='gray')   # predicted mask
   ```

## Notes

* Batch size: 64
* Predictions are grayscale masks
* Works on synthetic blob dataset
