================================================================
Authors : ANDREA MALARA

Summary of the code changes.
================================================================
DAY 02/06/2017
- Created the  directory "/scratch/malara/WorkingArea/backup/" where the is the original code updated to date.
- Created the directory "/scratch/malara/WorkingArea/HbbHbb_Run2-4b_2016/" where I modify the code. Every changes from the original file is made copying the original FILE as FILE_original and modifing FILE.
----------------------------------------------------------------
- Modified "/scratch/malara/WorkingArea/HbbHbb_Run2-4b_2016/AnalysisCode/PreselectedWithoutRegression/processPreSelection_Data.sh"
- Modified "/scratch/malara/WorkingArea/HbbHbb_Run2-4b_2016/AnalysisCode/PreselectedWithoutRegression/processPreSelection_Data.sh"
- Copies "libPhysicsToolsKinFitter.so" from "/cvmfs/cms.cern.ch/slc6_amd64_gcc530/cms/cmssw/CMSSW_8_0_25/lib/slc6_amd64_gcc530/libPhysicsToolsKinFitter.so" to "/scratch/malara/WorkingArea/HbbHbb_Run2-4b_2016/AnalysisCode/", because it was not the right version of ROOT.
- Modified "/scratch/malara/WorkingArea/HbbHbb_Run2-4b_2016/AnalysisCode/PreselectedWithoutRegression/LMRSelection/processLMRSelection_Data.c"
- Modified "/scratch/malara/WorkingArea/HbbHbb_Run2-4b_2016/AnalysisCode/PreselectedWithoutRegression/MMRSelection/processMMRSelection_Data.c"
- Modified "/scratch/malara/WorkingArea/HbbHbb_Run2-4b_2016/AnalysisCode/HbbHbb_MMRSelection.cc"
- Modified "/scratch/malara/WorkingArea/HbbHbb_Run2-4b_2016/AnalysisCode/PreselectedWithoutRegression/MeasureResolution/processMeasureResolution_Graviton.c"


================================================================
DAY 02/07/2017
- Modified "/scratch/malara/WorkingArea/HbbHbb_Run2-4b_2016/AnalysisCode/skimData.sh"
- Modified "/scratch/malara/WorkingArea/HbbHbb_Run2-4b_2016/AnalysisCode/Vskim.cc"
----------------------------------------------------------------
Description of the modification of "Vskim.cc"
The file now want as input the source and destination folder, the file name and inizial(InNum) and final(FinNum) progressive number: the program works for file such tree_(number).root in order to make a loop.
It provides a light skimming of input files [(Vtype == -1 || Vtype==4) && HLT_HH4bAll == 1].
Differently from the previous program, now it does HADD of all input files into a file named tree_total_from_(InNum)_to_(FinNum).root .
Some checks:
1 Verify the existence of input progressive file. Create a txt file to write down number file missing.
2 Not overwrite previous tree_total files, but moves them into tree_total_old files, warning of it.
----------------------------------------------------------------
----------------------------------------------------------------
- Created "/scratch/malara/WorkingArea/IO_file" folder where to put input and output files
- Modified file "/scratch/malara/crab_sub/crab_status.sh" copied from "/scratch/malara/WorkingArea/CMSSW_8_0_25/src/VHbbAnalysis/Heppy/test/crab/crab_status.sh". Add --maxjobruntime=2000 to enlarge runtime. Add "source /cvmfs/cms.cern.ch/crab3/crab.sh"
-
================================================================

