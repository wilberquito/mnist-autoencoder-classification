# Autoencoder Feature Extraction for Classification

Autoencoders are a type of neural network which generates an “n-layer” coding
of the given input and attempts to reconstruct the input using the code
generated.

The Autoencoder architecture architecture is divided into the encoder
structure, the decoder structure, and the latent space, also known as the
“bottleneck”.

## Encoder

$$h = E(x)$$

## Decoder

$$x' = D(h)$$

## Latence space

This is the data representation or the low-level, compressed representation of
the model’s input. The decoder structure uses this low-dimensional form of data
to reconstruct the input. It is represented by $h$.

## Self Supervised Learning

### pretext task

Now for both model to learn, we need a metric. This metric of loss $L$ which
should mesure how good the decoder $D$ does reconstructing the original data
from the encoder $E$.

$$L = Loss(x, x')$$

### downstream task

The learned representation by encoder $E$ can be used and fine tunned. As
encoder $E$ "knows" important features from the SSL problem, we can use it for
transfer learning in a classification or regression task.
