# Assignment-7
## Reciptive filed calculation for Inception model

| Layer | Feature map | Reciptive Field |Jump |
| --- | --- | --- | --- |
| Conv(7x7) S=2 | 112x112x64 | 7x7 | 1 |
| MaxPool(3x3) S=2 | 56x56 | 11x11 | 2 |
| Conv(3x3) S=1 | 56x56 | 19x19 | 4 |
| MaxPool(3x3) S=2 | 28x28 | 27x27 | 4 | 
| 3(a) Conv(5x5) S=1 | 28x28 | 59x59 | 8 |
| 3(b) Conv(5x5) S=1 | 28x28 | 91x91 | 8 |
| MaxPool(3x3) S=2 | 14x14 | 107x107 | 8 |
| 4(a) Conv(5x5) S=1 | 14x14 | 171x171 | 16 |
| 4(b) Conv(5x5) S=1 | 14x14 | 235x235 | 16 |
| 4(c) Conv(5x5) S=1 | 14x14 | 299x299 | 16 |
| 4(d) Conv(5x5) S=1 | 14x14 | 364x364 | 16 |
| 4(e) Conv(5x5) S=1 | 14x14 | 427x427 | 16 |
| MaxPool(3x3) S=2 | 7x7 | 459x459 | 16 |
| 5(a) Conv(5x5) S=1 | 7x7 | 587x587 | 32 |
| 5(b) Conv(5x5) S=1 | 7x7 | 715x715 | 32 |
| Conv(7x7) S=2 | 1x1 | 907x907 | 32 |


For **Inception block**, we have considered the maximum receptive field among the parallel branch, which is the branch with 5x5 convolution layer. So, for all Inception blocks in the above model, the Receptive filed calculation will be similar,  multiply (5-1) which is 4 with the corresponding jump value from the table and add it to the previous receptive field.

The Final(after AveragePool) **1x1** feature map activation can see **907x907** region of the input image. It is strange that the input image is only 224x224, but the receptive field of the final feature map activations are able to see a much bigger image region.

This architectural model will help us in learning images with incomplete objects covering entire image size with missing parts of the object, where with much larger receptive filed the network will be able to learn or hallucinate missing parts of the object.

Consider the example where the cat's face is only capture in the image and the other body parts are not seen for this it needs the receptive field much bigger than the input image to accurately classify the object in the image this is the case because the model would bhave been trained on the regular images of the objects which is in this case the full image of the cats.
