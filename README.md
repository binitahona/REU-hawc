# REU-hawc
Instructions for HAWC analysis using threeML software. References:  https://threeml.readthedocs.io/ , https://astromodels.readthedocs.io/ and https://data.hawc-observatory.org/datasets/crab_data/index.php .

#The threeML, astromodels and hawc hal has already been installed using the instructions listed in https://github.com/threeML/hawc_hal. To source the conda environment with all the packages.

1) export PATH="$HOME/miniconda3/bin:$PATH"

2) source activate new_hal #activate the new_hal environment

3) export OMP_NUM_THREADS=1

4) export MKL_NUM_THREADS=1

5) export NUMEXPR_NUM_THREADS=1

#Provide the data (HAWC_9bin_507days_crab_data.hd5) and response file name(HAWC_9bin_507days_crab_response.hd5) in

1) cd crab_9bin_507days

2) vi crab_fit_logparabola.py   # will open the .py file, after adding files to save the edits and close, use :wq

#Create a directory for results
mkdir results

#run the threeMl script
python crab_fit_logparabola.py
