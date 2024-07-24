======================
Dynamic Selection 
======================

------------------------------------------------------------------------------- 

Dynamic Ensemble Selection (DES)
------------------------ 

.. code-block:: python  

  class infodesreg.des.DES(self, pool_regressors=None, feature_subsets=None, k=7, knn_metric='minkowski', metrics='mse', threshold=0.2) 
                        
Dynamic Ensemble Selection (DES) is a method for improving the performance of ensemble learning by dynamically selecting a subset of base regressors that are most competent in predicting a given test sample. The selection is based on the performance of each regressor in the region of competence, which is determined using the k-NN algorithm.  

**Parameters**

        pool_regressors : list of regressors (Default = None)
                The generated_pool of regressors trained for the corresponding
                regression problem. Each base regressors should support the method
                "predict". If None, then the pool of regressors is a bagging
                regressor.

        k : int (Default = 7)
                Number of neighbors used to estimate the competence of the base
                regressors. 
                
        knn_metric: str or callable {'minkowski', 'cosine', 'manhattan', 'euclidean'}  (Default = 'minkowski') 
                The metric used by the k-NN to estimate distances. 

        metrics : str or callable {'mse', 'mape'} (Default = 'mape')  
                The parameter defines how the competence of regression models is measured within the RoC. This metric determines the criteria used to                  evaluate the performance of models and guide selection decisions. 

        threshold : float (Default = 0.1) 
                The parameter sets the threshold for model selection based on competence scores within the RoC. For example, a threshold of 0.1 means                  that models with a Mean Absolute Percentage Error (MAPE) of less than 0.1 within the RoC will be selected


------------------------------------------------------------------------------- 

Dynamic Regressor Selection (DRS) 
------------------------ 

.. code-block:: python  

  class infodesreg.des.DRS(self, pool_regressors=None, feature_subsets=None, k=7, knn_metric='minkowski') 
                        
Dynamic Regressor Selection (DRS) is a technique used in machine learning ensembles, where the most appropriate regressor or a subset of regressors is selected for each new sample to be predicted. This is done dynamically, based on the characteristics of the input data, with the goal of improving the overall regression performance of the ensemble. DRS algorithms typically use measures of regressor competence, which are estimates of the MAPE of each regressor for the given input data, to decide which single regressor to use. 

**Parameters**

        pool_regressors : list of regressors (Default = None)
                The generated_pool of regressors trained for the corresponding
                regression problem. Each base regressor should support the method
                "predict". If None, then the pool of regressors is a bagging
                regressor.

        k : int (Default = 7)
                Number of neighbors used to estimate the competence of the base
                regressors. 
        
                
        knn_metric : str or callable {'minkowski', 'cosine', 'manhattan', 'euclidean'}  (Default = 'minkowski') 
                The metric used by the k-NN to estimate distances. 
                
------------------------------------------------------------------------------- 
