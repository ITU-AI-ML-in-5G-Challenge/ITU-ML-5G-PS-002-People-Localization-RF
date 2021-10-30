#Assumption#
1) Testing data folder name is of format "snr18", "snr0" or "snr-18"

#Instructions#
1) Start with "Final.py" file execution
2) Input Parent folder path for testing data
    **Parent folder - Folder containing the testing data folders and the files(Final.py, NN_model.py, PreProcessing.py, Counting.py and tx.mat) 
3) Input the snr value for which testing needs to be done.

#Results#
** Final result would be generated and stored in .txt 
     - Naming format: mlResult(snr_val).txt
     - Example filename: mlResult18.txt
    
    
#Codeflow#
**This section is not required for results generation and code file execution.

1) Testing dataset would be loaded from the parent folder, given as input by the user (in Final.py)
2) PreProcessing.py would be called from Final.py and dataset pre-processing would be done to convert it 
   in the ML model input format.
3) After preprocessing trained model weights for localization and people counting would be loaded from NN_model.py 
   and Counting.py resperctively (these 2 python scripts are called internally in Final.py file).
4) Once trained weights are loaded Testing would be carried out on the preprocessed testing data via "Testing"
   function written in Final.py and number of people present in each sector would be predicted
5) Using the prediction vector for number of people in each sector, text file would be generated in "sector_form" funtion.
6) This .txt file will contain strings where each character represents one sector.
7) Strings are generated after combining the prediction results of both localization and people counting model (in "sector_num" function).
