1) After sending the first commit, it's sent in the index (origin/master)
2) After merging dev into master, master contains the same files than previously, and dev branch files. There's no conflict.
3) There's a conflict after merging dev2 into master because the bold.txt is different
4) In order to settle this problem, we suggest to put the same content in the two files 
5) After changing the content of bold.txt in R1, it doesn't change in R2 because it is not merged yet
6) We've to Fetch the new informations R1 into R2 then merge them to get them similar
7) it's refused because the file bold.txt in local repository is different from the one in remote
8) after modifying the file in R1 repository we cannot push it to the github, because it doesn't contain the new modifications of the bold files pushed before from R3. the solution is to pull the modifications from github, then change them and then push back to github
