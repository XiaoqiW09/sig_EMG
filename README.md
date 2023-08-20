### here includes the pipeline for using signature to classify or regress
the main function is 
auto(X_train = X_train, X_test = X_test, y_train = y_train, y_test = y_test, 
                        dataset, method, sig_level = 2,  
                        scale, time_aug,
                        bins_before, bins_after , bins_current,
                        file_path = './results/')
for classification：

  the input:
  X_train and X_test should be in shape (num_samples, num_timestamps, num_features)
  y_train and y_test should be in shape (num_samples,)
  dataset 
  

  
