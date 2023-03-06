# Siamese-Network-for-voice-pair-matching (Name Calling)

#### The main features of a audio signal
- MFCC (Mel-Frequency Cepstral Coefficients)
- Mel Spectogram
-  Zero-crossing rate
- Spectral-roll off
- Spectral flux
- Chroma features
## MFCC and Mel Spectogram Feature
#### The MFCC feature extraction technique basically includes windowing the signal, applying the DFT, taking the log of the magnitude, and then warping the frequencies on a Mel scale, followed by applying the inverse DCT. MFCC is a very compressible representation, often using just 20 or 13 coefficients instead of 32-64 bands in Mel spectrogram.
![mfcc](https://user-images.githubusercontent.com/53303541/128922693-cf6f6dba-06bd-4836-9586-d6575a00d931.jpeg)
                                                            
                                                        img src('Towards Data Science')
                                                        
#### MFCC
![anmol7_mfcc](https://user-images.githubusercontent.com/53303541/128305542-eb766c39-7a12-4e87-9f7c-008ce98c4dad.png)


#### Mel Spectogram
![mel](https://user-images.githubusercontent.com/53303541/128305659-9409cd26-e77a-4dea-b834-71a1e29aff07.png)

## Positive-Negative training testing pairs
When training siamese networks we need to have positive pairs and negative pairs:

#### Positive pairs: Two images that belong to the same class (ex., two images of the same person, two examples of the same signature, etc.)
#### Negative pairs: Two images that belong to different classes (ex., two images of different people, two examples of different signatures, etc.)
![pn](https://user-images.githubusercontent.com/53303541/128925227-27c712d7-abe5-40ea-beba-83d0f98ca3aa.png)


## Euclidean Distance function and Constrastive loss function
Let (X1, X2) be the input image pair, Gw be the function mapping producing low dimensional representations(where w represents the parameters), Y be the ground truth label denoting similar or not and Dw represents the euclidean distance.
![cl](https://user-images.githubusercontent.com/53303541/128926857-3476dd3d-6048-4c3c-8842-cc27b22131c5.png)

Contrastive loss bear a resemblance to the traditional cross entropy loss. The first term in the loss function takes care of similar pairs(Y=0) such that Dw becomes 0. The second term takes care of dissimilar pairs(Y=1) such that Dw becomes at least m.
![clt](https://user-images.githubusercontent.com/53303541/128927212-22caa618-55f8-4bff-b17a-1ac3f47ae4bd.png)


## Working of Siamese Network.
![Siamese-network-for-embedding-the-feature-maps-into-a-constant-vector](https://user-images.githubusercontent.com/53303541/128300246-2fdd584d-c237-44e2-927f-013797980b5c.png)
                                                                          
        Image src "ResearchGate"

Siamese, as the name suggests, comes from ‘Siamese Twins’, where we use two or more network(here, CNN in the case of images) which uses shared weights with intention to learn similarity and dissimilarity between images. The network outputs an n-dimensional embedding where each direction represents some visual pattern of the image.

## Base CNN model artchitecture
![base_model](https://user-images.githubusercontent.com/53303541/128301744-b59dc538-1261-4c00-b874-f82631279d85.png)

## Siamese Model artchitecture
![siamese](https://user-images.githubusercontent.com/53303541/128301830-7d007846-1575-4a68-8543-f57ebc55767a.png)

## Accuracy and Loss
![training](https://user-images.githubusercontent.com/53303541/128306128-e578579d-120b-4a9e-b3b8-5a4148c114e6.png)
![testing](https://user-images.githubusercontent.com/53303541/128306136-bac2408f-d156-4c17-8c95-d917ad8468c3.png)
