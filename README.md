# Detailed user guide on how to run this code:
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------
This code is used for image captioning on the flikr8k dataset (although it can be used on any dataset processed to have the same structure).  

To run this code, simply download the files off of this repository (including images/captions). Next, adjust your file paths within train.py
and getloader.py to align with your file locations for 'images' and 'captions.txt'.  

From there, simply adjust hyperparameters (listed below) and see how the captioning is able to perform!  
Hyperparameters (found in train.py):  
train_CNN -- True (for best performance!)  
load_model -- True (to load past progress with training)  
save_model -- True (to save the model's weights after each epoch)  
Embedding layers -- 256 (original)  
Hidden layers -- 256 (original)  
Learning rate -- 3e-4 (original)  
Epochs -- 100 (original)  

After running the model myself, I found the best performance (for the limited number of epochs I was able to achieve used Google Colab's maximum 12 hour runtime)
to be found used these parameters:  
Embedding layers -- 256  
Hidden layers -- 256  
Learning rate -- 1e-4  
Epochs -- 20  

Other parameters that were tested (to less successful results):  
Embedding layers -- 128/64/32  
Hidden layers -- 128/64/32  
Learning rate -- 1e-3  
Epochs -- 20/15/10/5  

Additional Notes on how to run this code using Google Colab!  
Simply run the attached file 'AlternativeModel.ipynb' and change the runtime settings to use GPU  
First mount the code using the top cell  
Next, run the cell that changes the working directory and has an option to clone the repo  
***Run the git clone cell above if there are issues***  
Run the click.py file so your mouse keeps the session active across the runtime  

Working on implementing BLEU score!!
