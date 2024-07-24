Welcome to XAI-DESReg documentation!
===================================

XAI-DESReg is an open-source library focusing on implementing state-of-the-art techniques for dynamic regressor and ensemble selection. This project is under active development. Contributions are welcomed through its GitHub page: https://github.com/adv-panda/xai-desreg

.. note::

   This project is under active development.

Contents
--------

.. toctree::

   usage
   introduction
   api
   example

Example 
-------- 

.. code-block:: python  

   from xaidesreg.des import DES  
   
   pool_regressors = [regressor1, ..., regressorN]
   
   # Initialize the DS model
   des = DES(pool_regressors)
   
   # Fit the dynamic selection model
   des.fit(X_dsel, y_dsel) 
   
   # Predict new examples
   des.predict(X_test)
   
   # Check performance (based on MSE)
   des.score(X_test, y_test) 
