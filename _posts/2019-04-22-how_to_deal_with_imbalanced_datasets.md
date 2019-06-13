---
layout: post
title:      "How to Deal with Imbalanced Datasets"
date:       2019-04-22 20:50:25 +0000
permalink:  how_to_deal_with_imbalanced_datasets
---


A dataset in which one class is much more frequent than the other is called an imbalanced dataset. A classification model with an accuracy of 95% sounds impressive but this doesn’t take the class imbalance into account and whatever classification algorithm you apply will bias the prediction model towards the more common class.

### **What are the options?**

**Go back to preparation and cleaning**

* Missing values may be a special case.
* Check for manual entries or human errors (using ‘o’ for ‘0’; name variations: “Shakespeare” or “Shakespeare William” for  “William Shakespeare“)
* Analyze the database schema; it may have changed over the years and the system has not been updated.
* Look at the categorical data and see how you can reconfigure and compress it without affecting the common elements.

**Change the performance metrics**

Accuracy is not the metric to use in imbalanced data. Confusion matrix, ROC curves, F1 score are other metrics that can be used depending on the problem; false positives or false negatives sometimes have different consequences; make sure to select an evaluation metric accordingly.

**Resample**

Oversample or undersample. Some challenges are you may potentially discard useful information, which could be important for building the classifiers; if oversampling there is the possibility of over-fitting the training data.

**Create synthetic samples**

Randomly sample the attributes from instances in the minority class. ROSE and SMOTE are popular techniques.

**Try different algorithms**

Start with a simple model like Naïve Bayes and see how much you can understand, and then consider building more complex models such as random forests, decision trees or neural networks.

There are many more tactics to deal with imbalanced data but this is a good start. On thing to keep in mind is that while comparing prediction models built through a combination of techniques the Area under the ROC Curve is a good instrument in determining which model is superior to the others.
