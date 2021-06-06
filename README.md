# Viola Jones Face Detection
- This is the python implementation of CVPR 2001 paper titled `"Rapid Object Detection using Boosted Cascade of Simple Features"` by Paul Viola and Michael Jones.
- `Dataset Used`: The data used is described at http://cbcl.mit.edu/software-datasets/FaceData2.html, and downloaded from www.ai.mit.edu/courses/6.899/lectures/faces.tar.gz
- The pickle_files directory contains the following pickle files:
    - `xtrain.pickle`, `xtest.pickle`, `ytrain.pickle`, `ytest.pickle`: The pickle files containing the train and test data as numpy array
    - `featureValues.pickle`: Contains the feature values computed for each image on all the features
    - `selectedFeatures.pickle`: Contains the best features (top 10 percent) among all the features
    - `selectedFeatureVals.pickle`: Contains the feature values computed for each of the images on the selected features

## Results
- The hyperparameter T represents how many weak classifiers are used. The table below shows accuracy and f1 score for T=10, 15 and 50 on test data.

    | T | Accuracy | Precision |
    | ------ | ------ | ------ | 
    | 10 | 0.86866 | 0.87710 |
    | 15 | 0.87586 | 0.89841 |
    | 50 | 0.88277 | 0.89822 |

- The `accuracy` and `precision` for a cascaded classifier with 1, 3 and 10 classifiers in the 1st, 2nd and 3rd stages is `0.87932` and `0.91201` respectively.
