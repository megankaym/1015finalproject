Motivation

Urinary tract infections (UTIs) are the most common outpatient infections, with a lifetime incidence of 50−60% in adult women. They represent anywhere from 1% to 6% of all medical visits in the US1. Symptoms include increased frequency and urgency to urinate, burning sensation while urinating, and/or cloudy, discolored urine. This bacterial infection strongly interferes with everyday life, and the impacts of UTIs reach beyond physical pain and irritation. Recurrent UTIs are associated with symptoms of anxiety and depression1. Resulting consequences include things such as financial burden, an inability to participate in activities or focus, and reduced quality of life. If treatment is not available, effective, or accessible, a UTI can infect the kidneys, indicated by fever and pain in the lower back, causing pyelonephritis.

Why use machine learning to predict antibiotic resistance based on the present organism? Machine learning is a great tool for personalized medical care. Extracting important information from massive amounts of data saves time and can produce useful insights. Deep learning is a lot of black box stuff, so for clinical data it's better to use simpler models. That way, clinicians with less of a computational background still know what is being done with this medical data. For this project, a random forest classification model was chosen.

Background

There are different types of UTIs. An uncomplicated UTI is when the kidney is normally functioning, there are no diseases like herpes, gonorrhea, or chlamydia that promote UTIs2, and there are no relevant functional or anatomical abnormalities in the urinary tract1. An acute uncomplicated cystitis is when symptoms only involve the lower urinary tract, whereas an acute uncomplicated pyelonephritis is when symptoms reside in the upper urinary tract. An asymptomatic bacteriuria is a positive urinary culture but an absence of symptoms. A recurrent uncomplicated UTI is the occurrence of 2 or more symptomatic episodes in a 6 month timespan, or 3 or more symptomatic episodes within a 12 month timespan. 

Treatment usually includes general antibiotics, and if symptoms persist a more detailed culture is done to target specific infecting organisms. Ideally, this detailed culture is done first but healthcare professionals seek umbrella treatments, which, when it comes to antibiotics, may cause resistance issues later on. A machine learning model that considers patient history (exposure to antibiotics) to determine if resistance is likely may prove a very helpful tool in addressing UTIs.

Data

The dataset(s) I have chosen for this project come from AMR-UTI at MIT: http://clinicalml.org/data/amr-dataset/. Request for access to files has been sent. I chose this data because I'm looking to do a project on women's health. I will develop a machine learning model that, based on previous antibiotic exposure and prior infecting organisms, predicts how likely it is for women of ages 18-25 (white or non-white) with no prior procedures to develop resistance. I will use all 3 data files (all_prescriptions.csv, all_uti_resist_labels.csv, all_uti_features.csv).


Aim 1: Build random forest classification model
Select relevant data for use
Combine multiple datasets into 1 using the common (anonymous) ID
Split data into training and testing


Aim 2: Extract predictions from random forest model
Run model to generate predictions on real data
Run model to generate predictions on fake (shuffled) data


Aim 3: Evaluate predictions
Model accuracies
Use a confusion matrix to determine TP, FP, TN, FN


Results
The model accuracy on the real data was 67.7%, and 69.1% on the shuffled data. 


Future work

This project could be extended by testing different types of models, such as SVM or K-NN. In addition, refining the prediction accuracies for specific resistances could improve accuracy (ie. NIT and NIT CIP resistance both contain NIT resistance, so the model would be partially correct in detecting NIT). Lastly, collecting and using data on other potential confounders such as diet and genetic predisposition could help the model make better predictions.


References

“An introduction to the epidemiology and burden of urinary tract infections.” 2019. NCBI. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6502976/.
“Urinary tract infection (UTI) - Symptoms and causes.” n.d. Mayo Clinic. Accessed July 20, 2023. https://www.mayoclinic.org/diseases-conditions/urinary-tract-infection/symptoms-causes/syc-20353447.
Sontag, David. “Amr-UTI: Antimicrobial Resistance in Urinary Tract Infections Dataset.” MIT Clinical ML, clinicalml.org/data/amr-dataset/. Accessed 24 Aug. 2023. http://clinicalml.org/data/amr-dataset/
