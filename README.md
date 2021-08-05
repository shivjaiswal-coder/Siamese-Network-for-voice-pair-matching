# Siamese-Network-for-voice-pair-matching

## mfcc and mel Spectogram feature
### mfcc
![anmol7_mfcc](https://user-images.githubusercontent.com/53303541/128305542-eb766c39-7a12-4e87-9f7c-008ce98c4dad.png)
### mel Spectogram
![mel](https://user-images.githubusercontent.com/53303541/128305659-9409cd26-e77a-4dea-b834-71a1e29aff07.png)



## Working of Siamese Network.
![Siamese-network-for-embedding-the-feature-maps-into-a-constant-vector](https://user-images.githubusercontent.com/53303541/128300246-2fdd584d-c237-44e2-927f-013797980b5c.png)
                                                                          
        Image src "ResearchGate"

Siamese, as the name suggests, comes from ‘Siamese Twins’, where we use two or more network(here, CNN in the case of images) which uses shared weights with intention to learn similarity and dissimilarity between images. The network outputs an n-dimensional embedding where each direction represents some visual pattern of the image.

## Base CNN model artchitecture
![base_model](https://user-images.githubusercontent.com/53303541/128301744-b59dc538-1261-4c00-b874-f82631279d85.png)

## Siamese Model artchitecture
![siamese](https://user-images.githubusercontent.com/53303541/128301830-7d007846-1575-4a68-8543-f57ebc55767a.png)
