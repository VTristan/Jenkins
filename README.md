# Jenkins

=> programmer, enchainer et automatiser des tâches (jobs)
=> pipeline d'intégration continue (build / run / test)
=> utilisé en devops





L'intégration continue (CI) 
=> exécution automatisée des tests 
=> gestion des builds
=> la gestion des versions
=> l'automatisation du déploiement 

# organization folders 

# multibranch Pipelines 

# Pipeline 



http://localhost:8181/github-webhook/

plugins!

créer/affecter des roles par users

trigger : sur echec/reussite/chaque cas:
rendre les jobs dépendants les uns avec les autres
ou remote url
trigger commit

cron : Heures, jours, périodes ...

maven => test


#Configuration as Code


#Desired Jenkins configuration
#password in enviroment variables

#job_dsl.groovy

#plugins
-cloudbees-folder
-configuration-as-code
-credentials
-github
-instance-identity
-job-dsl
-script-security
-structs
-role-strategy
-ws-clea


#The instance must be configured with a system message saying:
#Welcome to the Chocolatine-Powered Marvin Jenkins Instance

Signing up must be disallowed.
✓ A user named Hugo must be created and has:
– an id chocolateen;
– a password given by the USER_CHOCOLATEEN_PASSWORD environment variable.
✓ A user named Garance must be created and has:
– an id vaugie_g;
– a password given by the USER_VAUGIE_G_PASSWORD environment variable.
✓ A user named Jeremy must be created and has:
– an id i_dont_know;
– a password given by the USER_I_DONT_KNOW_PASSWORD environment variable.
✓ A user named Nassim must be created and has:
– an id nasso;
– a password given by the USER_NASSO_PASSWORD environment variable


The authorization strategy must be role-based.
✓ A global role named admin must be created and:
– has a “Marvin master” description;
– has all the permissions;
– is assigned to Hugo

A global role named ape must be created and:
– has a “Pedagogical team member” description;
– can build a job and see their workspaces;
– is assigned to Jeremy.
✓ A global role named gorilla must be created and:
– has a “Group Obsessively Researching Innovation Linked to Learning and Accomplishment” description;
– has the same permissions as the ape role, plus:
* the ability to create, configure, delete and move a job,
* cancel builds;
– is assigned to Garance.
✓ A global role named assist must be created and:
– has a “Assistant” description;
– can only view jobs and their workspaces;
– is assigned to Nassim.


folder "Tools" 
description : Folder for miscellaneous tools.


clone-repository
✓ Is named clone-repository.
✓ Is in the Tools folder.
✓ Has a GIT_REPOSITORY_URL string parameter with a “Git URL of the repository to clone” description
and no default value.
✓ When executed, clone with Git the repository at the specified URL, using a single shell command.
✓ Performs a pre-build workspace cleanup.
✓ Is only executed manually.
SEED
✓ Is named SEED.
✓ Is in the Tools folder.
✓ Has the following string parameters with no default values:
– GITHUB_NAME with a “GitHub repository owner/repo_name (e.g.: "EpitechIT31000/chocolatine")” description;
– DISPLAY_NAME with a “Display name for the job” description;
✓ When executed, create a job with the specifications listed below, using a single job_dsl.groovy
file script execution.
✓ Is only executed manually.
6
Jobs created by the SEED job
The following specifications apply to all the jobs that are to be created by the SEED job.
✓ Are at root.
✓ Are named according to the value of the DISPLAY_NAME parameter.
✓ Have a GitHub project property pointing at the repository specified by the value of the
GITHUB_NAME parameter.
✓ Have no parameters.
✓ Are only executed either by:
– a SCM poll triggered every minute (which starts a build if there are changes since the
last one);
– manual trigger.
✓ Use the prebuilt Git SCM system to automatically get the GitHub repository given by the
value of the GITHUB_NAME parameter.
✓ Perform a pre-build workspace cleanup.
✓ When executed, launch each of the following commands in separate shell script steps:
– make fclean
– make
– make tests_run
– make clean







