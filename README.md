# Machine Learning for Signal Processing 
##  HW1: Camera Pipeline
- Given the raw image(.nef), convert it into an image that can be displayed on a computer screen. 
- Use any methods to make the image look good. For example, do color space correction, brightness adjustment, white balancing, etc. 

> Reference:   
> This assignment and the given image actually refer to the website. (https://web.cs.hacettepe.edu.tr/~erkut/bbm444.s22/assignments.html)     
> A detailed implementation guideline (https://web.cs.hacettepe.edu.tr/~erkut/bbm444.s22/assgns/assgn1.pdf) from the website.      
> The testing images can be found at https://web.cs.hacettepe.edu.tr/~erkut/bbm444.s22/assgns/assgn1-data.zip

## HW2: Dimension Reduction
1. PCA   
   Given a 1D time series data, and split the signal into multiple segments with sliding window mechanism and the window size = 100, stride=1(for example, the data is [x, x+1, … x+k], 
and you need to split them as [[x, x+1, …, x+99], [x+1, x+2, …, x+100] ……]), implement PCA on your own (calling PCA packages is not allowed) on the signal segments. Show 
the eigenvector result in PCA and describe the relation with DCT. 
2. Autoencoder    
   Autoencoder is a dimension reduction method in deep learning, and it can be directly related to PCA. Mathematically, minimizing the reconstruction error in a constraint 
Autoencoder is the same as conducting PCA. If we use Autoencoder to approximate PCA, Autoencoder need to satisfy 4 constraints. 
    - Tied Weights: equal weights on Encoder and the corresponding Decoder layer. 
    - Orthogonal weights: each weight vector is independent of others. 
    - Uncorrelated features: outputs of the encoding layer are not correlated. 
    - Unit Norm: the weights on a layer have unit norm.   
    
    Implement Autoencoder architecture (one linear layer for encoder and decoder without bias, and batch norm layer, activated function) following the constraint to design the loss 
function, and train the model with data same as Q1. Show the weight and hidden layer results in encoder and compare with PCA result
