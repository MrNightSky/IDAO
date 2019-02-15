# IDAO
Here I show the decision of our team - HardNet of International Data Analysis Olympiad (https://idao.world)
We just do the task A (and private part B), where we need check only submisions by csv files. We had 17 place (score = 7605.64) on public and 23 (score = 7702.21) on private liderboard.
You can find describe of online stage problem here: https://docs.google.com/document/d/1ur3EdTo49PCYtbwN35IXVGV-0dR9X0U8TH3dZ4pT8JM/edit

In these repository you will find the next files:

    - FinalDecision.ipynb - jupyter notebook file with our last decision
    - HDFcreation.ipynb - jupyter notebook with creation of new features and clear hdf files, wich are needed in FinalDecision.ipynb
    - scoring.py - file from baseline of organizers with some specific scoring function
    - utils.py - also file from baseline with function of creation of new features wich are created in file HDFcreation.ipynb
    - features.npy - array of all features names
    - add_features.npy - array of features names wich are in train but absent in test

We have a very simple decision. We just tuned some parameters of LGBMClassifier (better score and speed of train compare with XGB and CatBoost). Then we divide all data by station wich have create it and divide all data to muon/pion and muon/proton then we train 6 independant models, wich are the same parameters and take the mean prediction of all of them.

To use this decision you need data from https://yadi.sk/d/pdwdp4Lt5X4DMQ