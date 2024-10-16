Scripts for statistical processing of patient and simulated datas for the article Transition to seizure in focal epilepsy: from SEEG phenomenology to underlying mechanisms" for publication in Epilepsia

Execute in order of cells.

For all questions, contact me on github, or by mail at mehmet-alihan dot kayabas at inserm dot fr or the corresponding author "Fabrice Wendling"

Inputs for patients: 
- for each patient, three lists of h² values for each comparisons of the three selected channels (i.e. channel 1 vs 2, channel 1 vs 3 and channel 2 vs 3) => 'patients/','*.dat' files
- timestamps of start and end of preictal, fast-onset and ictal periods => 'patients/timestamps_patient.csv'
- power values at each subbands (theta, alpha, beta and gamma) => 'patients/psd_subbands_data_out.csv'
- Names of the three SEEG electrode channels selected  => 'patients/montage_data/'
Simulations are performed on Coalia software. 
h² values and power values are calculated on Amadeus software.


Inputs for simulations:
- for each of the ten simulations, two lists of h² values (channel 1 vs 2 and channel 2 vs 1). In the script we take the average of the $h^2_{1,2}$ and $h^2_{2,1}$ as the focus of the study was not directionality. => 'simulations/h2_simus/'
- power values at each subbands (thet,a alpha, beta and gamma) => 'simulations/power_simu_data.csv'
- firing rates of the pyramidal cells and PV interneurons => 'simulations/PSPout_EXC.txt' 
    - (for figure 5) corresponding simulated timeseries for the firing rates => 'simulations/phase_value.dat'
    
NB1: In the scripts, FOA (fast-onset activity) period is interchangeably written as LVF (low-voltage fast).

NB2: Some simulation results might vary due to stochasticity (external input, the seed of RNG). The general h² synchronization pattern remains valid: Correlation during preictal phase, followed by a decorrelation at FOA followed by a correlation during the ictal phase.
