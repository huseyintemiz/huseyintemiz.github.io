Gaussian Blendshapes – In Depth

1. Traditional Blendshapes Recap

In classic 3D animation, blendshapes (also called morph targets) are:

A set of predefined 3D facial shapes, like smiling, blinking, frowning, etc.

A facial expression is created by linearly combining these shapes:



where  are the blendshape weights.

2. Adding Gaussians to Blendshapes

Now, the "Gaussian" part comes in to enhance this model. This can be done in several ways, but commonly involves:

A. Statistical Modeling of Blendshape Weights

Instead of fixed blendshape weights , we model them as coming from a multivariate Gaussian distribution:



This allows:

Regularization: Prevent unrealistic expressions

Sampling: Generate novel or personalized expressions

Learning: Fit weights to observed expressions using probabilistic methods

B. Latent Space Encoding

We can also learn a low-dimensional latent Gaussian space  and decode it into blendshape weights:



This is similar to a Variational Autoencoder (VAE) approach and allows for:

Smooth interpolation between expressions

Dimensionality reduction

Personalization via latent embeddings

C. Gaussian Representation of Landmarks or Deformations

Some methods go even further by:

Representing facial landmarks or vertex deformations as Gaussians in spatial or temporal space.

For example, modeling how a certain facial region deforms during speech as a trajectory in Gaussian space.

🎯 Why Use Gaussians in Blendshapes?

Goal

How Gaussians Help

Compression

Represent many blendshapes via a latent Gaussian

Generalization

Avoid overfitting to specific facial types

Expression Sampling

Sample new expressions from the Gaussian prior

Smooth Interpolation

Continuous variation via latent space

Personalization

Use personalized mean/variance for new users

🧠 Example Use Case

A facial animation system that:

Learns a latent Gaussian space of expression styles from multiple actors

Decodes this into dynamic blendshape weights for real-time animation

Samples from this space to animate synthetic avatars or reconstruct expressions from video

Let me know if you’re referring to a specific paper or model (like DECA, FaceWarehouse, or others) — I can tailor the explanation to match that!