## Scrape Repo links from General Assembly DSI-SYD-2
#### Developed by : Srikanta Patra
##### Thanks to Joel Harlander for providing the idea to scrape the DSI repo   :).

* The code will scrape all available class lessons repo for DSI-SYD-2 git hub area and out put a git clone command for each link.
* You can copy the links and put into a file e.g. all_DSI_repo.sh (with bash shell #!/bin/bash at the beginning of the file)
* Run the command 'chmod u+x yourfilename.sh'
* Execute the sh file from a terminal ./yourfilename.sh
* This will clone all the repos in the current directory.

## Alternatively
* If you do not want to scrape it yourself, please download the file named "GA_DSI2_repo_clone.sh" in this git hub area to your local directory.
* Run the command 'chmod u+x GA_DSI2_repo_clone.sh'
* Execute the sh file from a terminal ./GA_DSI2_repo_clone.sh
* Feel free to modify the bash file and use a subset of clone commands if you want to.
* If you already have a set of clones and you just want to do a bulk pull, I found a command as below
* find . -name ".git" -type d | sed 's/\/.git//' |  xargs -P10 -I{} git -C {} pull
* Use the above command at your own risk ..... :). it will ask for your git SSH key, GA-DSI-SYD username and password and iteratively pull all the repo's. 
* Assumption: All your repo's are under a single root directory (doesn't matter at what level below the root)
