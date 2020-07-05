# PreTrainedImageClassifier-DogBreeds
Use a pre-trained image classifier to identify dog breeds

Determining the "best" classification algorithm works on correctly identifying a dog's breed:

Principal Objectives:
	
	1) Correctly identify which pet images are of dogs (even if breed is misclassified) and which pet images aren't of dogs.
 
	2) Correctly classify the breed of dog, for the images that are of dogs.
 
	3) Determine which CNN model architecture (ResNet, AlexNet, or VGG), "best" achieve the objectives 1 and 2.
 
	4) Consider the time resources required to best achieve objectives 1 and 2, and determine if an alternative solution would have given a "good enough" result, given the amount of time each of the algorithms take to run.

Based on the summary results below:

Objectives:
1) Classify "dogs" and "not-a-dog": VGG and AlexNet were able to classify at 100% accuracy

2) Classify "Breeds": VGG out performed both of the other architectures in this category with 93.33% accuracy

3) Based on the results, the "best" model architecture is VGG. 

4) VGG took more time to process the results but it gave the results with more accuracy in "correct dog breed" classification, 
   even though VGG and AlexNet are 100% accurate on "Is-a-Dog" and "Not-a-Dog" classification. 
   AlexNet took just 6 secs to process the results but with less accuracy in "Correct Breeds" category. 
   If we can get the individual times taken for 1 and 2 objectives then we can decide on which architecture is best in related to time performances 
   and if we can use different model for different objective.
   ResNet provided 100% accuracy in "Is-a-Dog" and 90% in "Correct Breed" and it took 1/6th of the time VGG took.


*** Results Summary for CNN Model Architectures VGG, ResNet, AlexNet ***
```
+----------------+--------------+------------------+
| # Total Images | # Dog Images | # Not Dog Images |
+----------------+--------------+------------------+
|       40       |      30      |        10        |
+----------------+--------------+------------------+
+------------------------+---------------------+----------------+------------------+----------------+
| CNN Model Architecture | % Not-A-Dog Correct | % Dogs Correct | % Breeds Correct | % Match Labels |
+------------------------+---------------------+----------------+------------------+----------------+
|          VGG           |        100.00       |     100.00     |      93.33       |     87.50      |
+------------------------+---------------------+----------------+------------------+----------------+
|         ResNet         |        90.00        |     100.00     |      90.00       |     82.50      |
+------------------------+---------------------+----------------+------------------+----------------+
|        AlexNet         |        100.00       |     100.00     |      80.00       |     75.00      |
+------------------------+---------------------+----------------+------------------+----------------+
```

Time taken to process the images:
```
+------------------------+---------------------+
| CNN Model Architecture | 	Time taken     |
+------------------------+---------------------+
|          VGG           |        0:1:6        |
+------------------------+---------------------+
|         ResNet         |        0:0:11       |
+------------------------+---------------------+
|        AlexNet         |        0:0:6        |
+------------------------+---------------------+
```

