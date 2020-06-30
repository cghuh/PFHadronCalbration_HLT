# PFHadronCalbration_HLT

How to use (examples)

## Recipe
    cmsrel CMSSW_11_1_0_pre6
    cd CMSSW_11_1_0_pre6/src/
    cmsenv
    git cms-merge-topic felicepantaleo:fix_realistic_sim_clusters_11_1_0_pre3
    git clone https://github.com/missirol/JMETriggerAnalysis.git -o missirol -b phase2
    git cms-addpkg HLTrigger
    git cms-addpkg RecoParticleFlow
    git cms-addpkg FastSimulation
    git clone https://github.com/cghuh/PFHCalib.git
    scram b -j4
    cd PFHCalib/PFHadHLT/python
    cmsRun PFHadCalib_cfg.py
