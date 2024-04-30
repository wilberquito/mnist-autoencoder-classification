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
to reconstruct the input. It is represented by `h`.

## Self Supervised Learning

Now we can use the encoder `E` and fine tunning it for a classification problem.
As encoder `E` "knows" important features for the SSL problem, we can apply
transfer learning for a classification or regression task.
