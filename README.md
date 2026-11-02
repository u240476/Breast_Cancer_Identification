Breast Cancer Classification with Decision Trees

This project uses the Breast Cancer Wisconsin (Diagnostic) dataset, which has 569 tumor samples described by 30 measurements of cell nuclei from digitized fine needle aspirate images. The goal is to classify each tumor as malignant or benign.

I trained a decision tree on a stratified 50% split and evaluated it on the held-out half. The default tree reached 0.912 accuracy but had six leaves containing a single sample, a sign of overfitting. Switching the split criterion from gini to entropy raised accuracy to 0.947 and produced a slightly simpler tree. I then tested min_samples_leaf values of 1, 5 and 10. A value of 5 gave the best accuracy, precision and F1 of the three (0.930, 0.934 and 0.923), while also producing a simpler tree.

The most important splits were on size and shape features such as worst concave points and worst radius, which fits what we’d expect for malignancy. With only 285 test samples, small differences between models may be noise. This is a learning project, not a diagnostic tool.
