### here includes the pipeline for using signature to classify or regress
the main function is 

auto(X_train, X_test, y_train, y_test, 
                        dataset, method, sig_level = 2,  
                        scale, time_aug,
                        bins_before, bins_after , bins_current,
                        file_path)
## for classification：

  ### the input:
  #### X_train and X_test:
  should be in shape (num_samples, num_timestamps, num_features)
  
  #### y_train and y_test:
  should be in shape (num_samples,)
  
  #### dataset 
  is the for file_name
  
  #### method 
  shoule be chosen from ['ts_knn','ts_svc','logisticregression','svc','knnclassifier','adaboostclassifier','randomforestclassifier']

  #### sig_level 
  is the level of signature you want to use

  #### scale: ['minmax','standard','None']
  'minmax' is for normalize scale
  
  'standard' is for standardize scale
  
  'None' is for no scale

  #### time_aug: [True,False]
  True is for using time as extra feature


  #### bins_before, bins_after, bins_current
  would not use in the classification case

  #### file_path
  the path to save the output csv


  ### the output
  the output will be *.csv file
  #### name
  {dataset} + {method} + {scale} + {timeaug} + {sig/flat}
  ##### dataset
  defined with parameter dataset

  ##### method
  defined with parameter method

  ##### scale
  show which scale used

  ##### timeaug
  _timeaug only shows when the time_aug is True

  ##### _sig/_flat
  _sig represents signature used

  _flat represent we flatten the (num_samples, num_timestamps, num_features) into (num_samples, num_timestamps*num_features)


  #### content
  there will be accuracy and time cost in the .csv file
  


  
  

  
  

  
