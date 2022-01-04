# Non Converging CNNs
Hi! 

First of all, thanks for helping me with debuggin this CNNs. 

The non convergence problem of the CNNs occur when I use the `F.interpolate()`/ `F.upsample()` functions from PyTorch for the autoencoder exercises (both the denoising and vanilla autoencoder). I use a relatively simple architectures with `mode='nearest'`. You can see both cases in:

- `Convolutional_Autoencoder_Exercise.ipynb`: the CNN that presents the problem can be found in the ***Interpolation Upsampling with Nearest Neighbors and Convolutions*** section.
- `Denoising_Autoencoder_Exercise.ipynb`

When the problem happens I'm training the CNN on a Nvidia GTX 1060 GPU (I also tried to train them on the CPU but the problem persisted). The only way I found to consistently solve the problem is to change the weight initialization method (you can uncomment the weight initialization method inside the `__init__` method of the nets to see this). 

However, at the beginning, I reinitiated the kernel for the `Convolutional_Autoencoder_Exercise.ipynb` CNN, without making further changes, and it worked and converged. 

Thanks again for helping me with this!
