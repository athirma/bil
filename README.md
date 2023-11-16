bil is a sequence prediction tool specializing in forecasting SARS-CoV-2 variants and essential amino acid substitutions within virus evolution. Its framework can be adapted for predicting mutations in other virus sequences given sufficient sequence data.

The tool comprises three primary sections:
1. bil code developed in Python (3.7) for training Bi-LSTM language models.

Package           Version       
-ip	          22.3	
jieba	          0.42.1	
numpy	          1.21.6	
torch	          1.12.1	
typing-extensions 4.4.0  	

2. Sequence generation code in MATLAB R2020b for generating SARS-CoV-2 variants (Used for Reproduction).
Restorethedataset1.m is the code to simulate and restore the SARS-CoV-2 variants in dataset1.
Restorethedataset2.m is the code to simulate and restore the SARS-CoV-2 variants in dataset2.
Predictionofthesequencesbyusingdataset1.m is the code to predict the SARS-CoV-2 variants based on dataset1.
Predictionofthesequencesbyusingdataset2.m is the code to predict the SARS-CoV-2 variants based on dataset2.

3. Figure drawing code in MATLAB R2020b.
Draw circles.m

The tool comprises several MATLAB mats:
1. dataset1.mat
2. dataset2.mat
3. pn1.mat is the occurance frequency of the dominant amino acid at each hotspot for dataset 1.
4. pn2.mat is the occurance frequency of the dominant amino acid at each hotspot for dataset 2.


Usage of bil
1. Download and save all the files (including the well-trained Bi-LSTM model), and set files to MATLAB path. The download/installation would not take more than a minute. 
2. Open the MATLAB file (e.g., "Restorethedataset1") and define model parameters: sequence generation number (num), mutation frequency of hotspots (alpha), and more mutable hotspot mutation frequency (h).

Demo:
Set the target dataset in MATLAB mat form, open the MATLAB file (e.g., "Restorethedataset1"), and change the dataset name to your own dataset's name. Next deine model parameters: sequence generation number (num), mutation frequency of hotspots (alpha), and more mutable hotspot mutation frequency (h). You should expect to obtain either the simulation result of your dataset (e.g., "Restorethedataset1") or the prediction of the new variants based on the input dataset (e.g., "Predictionofthesequencesbyusingdataset1"). The expected run time is based on the size of your input dataset.
