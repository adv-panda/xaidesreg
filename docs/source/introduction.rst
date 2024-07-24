====================
Introduction
====================

.. note::

  XAI-DESReg is open source library focusing the implementation of the state-of-the-art techniques for dynamic regressor and ensemble selection with late fusion setting. This project is under active development.


**Features & Uses**

**InfoDESReg has the following features:**

⭐️ **Support for diverse DS technques**. XAI-DESReg supports 1 dynamic regressor selection and 1 dynamic ensemble selection techniques. 

⭐️ **Explainable AI**. XAI-DESReg provides deep and suitable XAI for dynamic selection techniques.



**Infodeslib has a wide range of uses, including:**

✅ Providing various handy **metrics**; 



**Dynamic Ensemble Selection** 

Dynamic Ensemble Selection (DES) is a method for improving the performance of ensemble learning by dynamically selecting a subset of base regressor that are most competent in predicting a given test sample. The selection is based on the performance of each regressor in the region of competence, which is determined using k-NN algorithm. The DES approach aims to balance the accuracy and diversity of the selected ensemble of regressors to improve the overall prediction performance. 

.. image:: https://raw.githubusercontent.com/adv-panda/xaidesreg/main/docs/images/dynamic_regressor_pipeline.png
