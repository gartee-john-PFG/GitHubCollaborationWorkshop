# GitHubCollaborationWorkshop
Repo for GitHub - Collaborating with Your Team Workshop


## Exercise One - Cloning the repository
## Exercise Two - working collaboratively 
* Centralized Model
    * acts must like SVN or other server-based VCS
    * only a **_main_** branch
    * process
        * clone the repository
        * make your changes to **_main_**
        * to push
            * fetch current **_main_** with rebase
            * correct any conflicts
            * push your changes to **_main_** 
* Feature Branch Development
    * allows for independent development and managing origin
    * process
        * clone the repo
        * for each feature
            * create a **_branch_**
            * push **_branch to origin at will
                * fetch from **_main_**
                * checkout feature **_branch_**
                * rebase feature onto **_main_**
                * push the feature **_branch_** to origin
            * to apply your feature to **_main_**
                * generate a PR from your **_branch_** to **_main_** -or-
                * merge your up-to-date feature **_branch_** back to local **_main_** and push **_main_** (not recommended)
    * merge back into either **_develop_** or **_main_** branch
* Gitflow Workflow
    * **_develop_** branch
        * we operate off of the **_develop_** branch
        * feature branches are used
            * feature branches merge back to **_develop_**
            * feature branches are created off of latest **_develop_** commit
    * release 
        * when release is needed, create a release branch off of desired **_develop_** branch commit
            * this starts a new release cycle on **_develop_**
        * created from **_develop_** branch with tested features
        * only documentation, bug-fixes, and release-related commits added to the release branch
        * when release is complete, merge back to **_develop_** and **_main_**
        * delete the **_release_** branch
    * main branch
        * updated only from **_release_** or **_hotfix_** branches
        * **_hotfix_** immediately merged to **_main_** and **_develop_**/**_release_** branch
* Forking Workflow (open-source model)
    * every contributor forks the primary repo
    * clones forked [origin]
    * defines primary as remote [upstream]
    * push to [origin], PR to [upstream]
    * fetch from [upstream]
    * rebase/merge to local
    * push to [origin]
    * generally operates on feature branches
    * feature branches are sent to [upstream] in a PR
* Trunk-based development 
    *   only branch is **_main_**
    *   every commit goes to **_main_**
    *   requires high level of automated testing and feature tags

## Exercise 3 - When and When Not to Rebase  

