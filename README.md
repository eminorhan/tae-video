## Transformer autoencoder for videos (TAE-VID)

A simple transformer-based autoencoder model for videos.

- Encoder and decoder are both vanilla ViT models.
- The skeleton of the code is recycled from Facebook's [MAE-ST](https://github.com/facebookresearch/mae_st) repository with several simplifications.
- Work in progress.

### Why transformer-based autoencoders for videos?

- Better representational alignment with transformer models used in downstream tasks, *e.g.* diffusion transformers.
- It opens the door to training models on massively longer videos by trading off longer temporal context for massively reduced spatial size.
- Current "first stage models" used for image/video compression are too complicated, *e.g.* using adversarial losses (among others). I'd like to simplify this process by showing simple plain autoencoders are performant as first stage models.