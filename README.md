# AOS_LRE_Synch
#This repo has two sub folders

#scripts- where the vugen script and all files are contained
#tests- where the yaml file that is the LoadRunner Enterprise scenario is contained

#This repo is utilized in the 'LoadRunner Enterprise Git-YAML Synch' job in Jenkins
#This job will synchronize both the vugen script and the test (YAML file) with LoadRunner Enterprise running on NimbusWindows

#This repo is also utilized with another job in jenkins, 'LoadRunner Enterprise Performance Validation'
#This job clones the git repo containing the scripts and yaml test and create the scenario to be executed by LRE on the fly.

#Limitations:
#Because VuGen has limitations in committing to git repos (it can only commit to root), in order to make a change in VuGen and commit/push to this repo you will first
#need to clone this repo to local, then instead of doing a "commit" from VuGen, you will need to File>Save As to the local repo/scripts folder. Then using any Git UI tool
#or CLI, commit/push to the remote, in this case, this repo in the devops container
