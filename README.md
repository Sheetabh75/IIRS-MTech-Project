# IIRS-MTech-Project
<b><i>Final year MTech Project (2018-19) - CNN based species identification application</i></b><br/>
<br/>
This project was carried out for identification of species from following for super-classes: <br/>
1. Butterfly - 22 species
2. Protozoa - 5 species
3. Animalia - 5 species
4. Aves - 9 species <br/>
<br/>
<b>Step 1 :</b> Navigate to "MTech_Project" folder in home directory - "/home/sheetabhg/MTech_Project"<br/>
Separate folders are set-up for dataset, scripts and models for 4 different super-classes.<br/>
<br/>
<b>Step 2 :</b> Set up training and testing data in separate folder as below example <br />
<b>Butterfly images path:</b><br/>
Train - MTech_Project/Dataset/Butterfly/Train <br/>
Test - MTech_Project/Dataset/Butterfly/Test <br/>
<b>Aves images path:</b><br/>
Train - MTech_Project/Dataset/Aves/Train <br/>
Test - MTech_Project/Dataset/Aves/Test <br/>
<b>Animalia images path:</b><br/>
Train - MTech_Project/Dataset/Animalia/Train <br/>
Test - MTech_Project/Dataset/Animalia/Test <br/>
<b>Protozoa images path:</b><br/>
Train - MTech_Project/Dataset/Protozoa/Train <br/>
Test - MTech_Project/Dataset/Protozoa/Test <br/>
<br />
<b>Step 3 :</b> Create a conda environment using the "MainProject.yml" file and activate that environment. YML file is located in home directory "home/sheetabhg/"  <br/>
<br/>
<b>Step 4 :</b> Navigate to folder "MTech_Project/Scripts" where all the scripts exist. <br/>
For each super-class, 3 scripts are created - dataloader, cnnmodel, testmodel. <br/>
For example, <br/> 
<b>aves_dataloader.py :</b> Loads all the training & testing images, perform the pre-processing steps and create the tensors ready to be fed to CNN model. <br/>
<b>aves_cnnmodel.py :</b> In this script, CNN architecture of the model is defined along with the network input hyperparameters. The CNN model is trained using this script and the trained model is saved. <br/>
<b>aves_testmodel.py :</b> This scripts load the trained model in .h5 format. The path of the trained model is provided in load_model function. Model's performance is tested on new set of testing images stored in Test folders for respective super-classes mentioned in step 2. <br/> 
<br/>
<b>Step 5 :</b>  To start model training, run the script "aves_cnnmodel.py" to start training of CNN model. This script will import and run "aves_dataloader.py" script before running the "aves_cnnmodel.py" script. Similarily run cnnmodel scripts for other super-classes to start training.<br/> 
<br/>
<b>Step 6 :</b> In order to directly test the model using already trained and saved model file, directly run the script "aves_testmodel.py". Make sure to specify the correct path of saved model in load_model function in testmodel script. <br/>
Trained model files are located in folder "MTech_Project/Models".
<br/>

