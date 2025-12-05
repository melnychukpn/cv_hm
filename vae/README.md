# VAE Project - Training Results

## Autoencoder Compression Analysis

Training autoencoders with different latent dimensions on MNIST dataset.

### Results Summary

| Latent Dim | Final Test Loss (MSE) | Compression Ratio | Quality |
|------------|----------------------|-------------------|---------|
| 2 | 0.0357 | 392.0x | Poor |
| 8 | 0.0143 | 98.0x | Fair |
| 16 | 0.0083 | 49.0x | Good |
| 32 | 0.0051 | 24.5x | Very Good |
| 64 | 0.0043 | 12.2x | Excellent |
| 128 | 0.0041 | 6.1x | Near Perfect |

### Key Finding
**Smaller latent dimension = Higher compression but lower quality**

The sweet spot appears to be around **latent dim 64** with 12x compression and excellent reconstruction quality.

---

## VAE Training Results

Training Variational Autoencoder on MNIST Digits with latent dimension = 20.

### Training Progress

| Epoch | Total Loss | Reconstruction Loss | KL Divergence |
|-------|-----------|-------------------|---------------|
| 10 | 103.94 | 85.06 | 18.89 |
| 20 | 100.20 | 80.73 | 19.48 |
| 30 | 98.64 | 78.93 | 19.71 |
| 40 | 97.71 | 77.89 | 19.82 |
| 50 | 97.14 | 77.22 | 19.92 |

### Observations
- **Reconstruction loss** steadily decreases → Better image quality
- **KL divergence** stabilizes around 19-20 → Proper latent space regularization
- **Total loss** converges smoothly → Successful training

---

## Files
- `VAE_comprehensive.ipynb` - Complete implementation and experiments