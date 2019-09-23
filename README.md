# Cows-and-Folders-Challenge
Recursion and Trees 
Problem Description: In a folder system there are: -shared folders -confidential folders
Each folder has a list of cows that are explicit members of the folder. 
If you are an explicit member, you can access that folder and all its non-confidential child folders through ineritance

A folder is called a leaf if it is not the parent of any other folder. 
A cow is uncool if there is at least one leaf they cannot access. Determine which cows are uncool.

Input: 3 - Q cows 
2 1 - M shared folders, N confidential folders 
1 1 0 - folder id of shared, K cows have explicit access, K ids (M=2) 
2 1 1 - folder id of shared, K cows have explicit access, K ids (M=2) 
3 3 0 1 2 - folder id of confidential, K cows with explicit access, K ids 
2 - single non-negative int G 
1 2 - U,V. U folder id of parent, V child folder id (G=2) 
1 3 - U,V. U folder id of parent, V child folder id (G=2) 

Output: 
(Return ID of uncool cow, cow that cannot access at least one leaf) 
Cow 0 has access to SF1 id=1 (1 1 0) 
Cow 1 has access to SF2 id=2 (2 1 1) 
Cow 0 also has access because folder id=1 is a parent of folder id=2 (1 2) 
Cow 0,1,2 has access to CF3 id=3 (3 3 0 1 2) 
Cow 2 cannot access SF2 id=2, so return 
