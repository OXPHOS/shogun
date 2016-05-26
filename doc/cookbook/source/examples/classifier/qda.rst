===============================
Quadratic discriminant analysis
===============================

Quadratic discriminant analysis (QDA) is used to separate measurements of two or more classes of objects by a quadric surface.
For QDA, the class label :math:`y` is assumed to be quadratic in the measurements of obeservations :math:`X`, i.e.:

.. math::

    \mathbf{x^{T}Ax} + \mathbf{b^{T}x} + c

QDA is a generalisation of linear discriminant analysis (LDA).

-------
Example
-------

Imagine we have files with training and test data. We create CDenseFeatures (here 64 bit floats aka RealFeatures) and :sgclass:`CMulticlassLabels` as

.. sgexample:: qda.sg:create_features


We create an instance of the :sgclass:`CQDA` classifier with feature matrix and label list.
:sgclass:`CQDA` also has two default arguments, to set tolerance used in training and mark whether to store the within class covariances

.. sgexample:: qda.sg:create_instance

We run the train QDA algorithm and apply it to test data, which here gives :sgclass:`CMulticlassLabels`.

.. sgexample:: qda.sg:train_and_apply

We can evaluate test performance via e.g. :sgclass:`CMulticlassAccuracy`.

.. sgexample:: qda.sg:evaluate_accuracy


----------
References
----------

:wiki:`Quadratic_classifier`
:wiki:`Linear_discriminant_analysis`
