# Beauty Virtual Makeup Tryon:

## Environment:
Python 3.6
Tensorflow 1.x

## Prerequisites:
1. Download the trained BeautyGAN model weights from this link : https://drive.google.com/drive/folders/1J8vjyjaikPAXF9ln-2zvT8xkbM4c7QyM?usp=sharing  and make sure you are logged in into your google account
2. Place these weights in "model" folder

## Usage:
You can use the driver code given in the Myntra_Virtual_Makeup_Tryon.ipynb

## Credits:
This code is the implementation of this paper BeautyGAN: http://colalab.org/media/paper/BeautyGAN-camera-ready.pdf

There is no opensource code for this paper But there is a github repo : https://github.com/Honlan/BeautyGAN

This code has been taken from the specified repo.

## Implementation:
We have tried using SCGAN,PSGAN and BeautyGAN. But, BeautyGAN gave us consistent results among all of them. We can see that BeautyGAN is giving promising results.But, Sometimes the color of the product is being changed in the output. 

![Alt text](/assets/result_1.jpg?raw=true "Title")

![Alt text](/assets/result_shraddha.jpg?raw=true "Title")

## Future Work:
We can use BiSeNet which segments the output and input images. Then we can copy and paste the parts of input image on to the output image which should not be changed by the model.

# Beauty Recommendation System:

## Environment:
Python 3.6
Tensorflow 2.x
Transformers latest version

## Prerequisites:
1. Download the trained Sentiment Analysis model weights from this link : https://drive.google.com/file/d/1Nc7-IY62dFMtJLb117aZ9gZoEMnS-qNM/view?usp=sharing  and make sure you are logged in into your google account
2. Place these weights in "Sentiment_Analysis_Weights" folder

## Credits:
This implementation is purely done by us and we also used simple custom formula to take reviews,rating and also similarity into consideration

## Usage:
You can use the code given in the Myntra_Beauty_Product_Recommendation_System.ipynb

## Implementation:
We have used the T-distributed Stochastic Neighbor Embedding (t-SNE) for reducing the higher dimensional data of products and ingredients to lower dimensional (2D). We have then taken top 10-20 products which are closer to the required ingredients product(this will be prescribed by expert). Then we have used Sentiment Analysis to analyse the reviews of each product and will be giving a Critical Score which contanis SimilarityScore,Rating,ConfidenceScore of Sentiment Analysis.

Using this Critical Score we will be sorting the products and these are the final outputs.

Formula we used: CriticalScore = ConfidenceScore*10000 + ((Rating*1000)-(Similarity*1000))

Here: ConfidenceScore - Probability of SentimentClassifier Whether it is Positive or Negative

Here: Rating - Overall Rating of product in the website (between 0 and 5)

Here: Similarity - Distance between this product and reference product  

![Alt text](/assets/Beauty_Recommendation_1.PNG?raw=true "Title")
