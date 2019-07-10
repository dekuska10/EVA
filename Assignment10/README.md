# Assignment10


ϕi = ϕi−1 + 2^(η−τ) ∗ (Filter size − 1)

ϕi = receptive field of layer i
ϕi−1 = receptive field of layer i-1 (previous layer)
η = number of strided convolutions
τ = number of  deconvolutional layers

ϕi−1 = 29 
Filter size = 3 (according the paper all the layers having kernal of size 3)

η = 3 (from the table it is informed that 3 strided convolution before the current layer )
τ = 0 (since their is no deconvolution previous to this layer)


 = 29 + 2 ^ (3-0) * (3-1)
 = 29 + 16
 = 45
