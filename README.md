# miniAOD_example
https://twiki.cern.ch/twiki/bin/view/CMSPublic/WorkBookMiniAOD2015#Taus

go to link above, this file is created by cmsDriver.py miniAOD-prod -s PAT --eventcontent MINIAODSIM --runUnscheduled --mc --filein /store/relval/CMSSW_7_4_1/RelValTTbar_13/GEN-SIM-RECO/PU50ns_MCRUN2_74_V8_gensim71X-v1/00000/06ACC5B7-7FEC-E411-8CB1-0025905964BA.root --conditions MCRUN2_74_V8 -n 100 --no_exec

One way to keep AOD tau while keep all other info from miniAOD, to me, it may be viable, to run RECO_ggH first, then run a similar file like this, with change of outputCommands. Instead of use what is defaut, we need to add our tau tuples. 

https://github.com/cms-sw/cmssw/blob/CMSSW_8_1_X/Configuration/EventContent/python/EventContent_cff.py

cmsDriver.py miniAOD-prod -s PAT --eventcontent MINIAODSIM --runUnscheduled --mc --filein root://eoscms//eos/cms/store/user/mshi/heavyHiggs_300_light_9_2mu2tau_sim/heavyHiggs_300_light_9_2mu2tau_sim_NUM.root --conditions 76X_mcRun2_asymptotic_v12 -n 300 --no_exec
