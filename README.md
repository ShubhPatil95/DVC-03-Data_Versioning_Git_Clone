<h2> <a href="https://github.com/ShubhPatil95/DVC-03-Data_Versioning_Git_Clone"> DVC-03-Data_Versioning_Git_Clone</a></h2>

<p>
<strong> Here in this tutorial we will see how we can a take code and data.txt.dvc file from git and data.txt file from our remote storage</strong>
  
### Step1
* Create a folder under name DVC-03-Data_Versioning_Git_Clone
```ruby
mkdir DVC-03-Data_Versioning_Git_Clone
cd DVC-03-Data_Versioning_Git_Clone
```
### Step2  
* Now you are into DVC-03-Data_Versioning_Git_Clone folder. Lets clone the repository we used in second tutorial DVC-02-Data_Versioning
```ruby
git clone https://github.com/ShubhPatil95/DVC-02-Data_Versioning.git
```
### Step3  
* Go inside of folder DVC-02-Data_Versioning
```ruby
cd DVC-02-Data_Versioning
```  
### Step4  
* Now you can see there is only one file name data.txt.dvc and our datam file data.txt is not present
* Just run a command git pull and you will see data.txt file is present with sentence "This is third commit"
```ruby
dvc pull
cat data.txt
```   
### Step5
* Now let say you want to see how was your data at your first commit? Do follow below steps to check it
```ruby
git log --oneline  ## copy SHA ID of first commit, mine is 0b0d5ef
git checkout 0b0d5ef  ## checkout to first commit
cat data.txt  ## although you checkout to first commit but still your data.txt is showing data of third commit
dvc pull   ## This command will pull your data of first commit from remote storage
cat data.txt  ## you can see now data is updated with first commit
```  
### Step6
* You can again back to last commit, by checkout to branch name 
```ruby
git checkout main
cat data.txt   ## but data is still showing of first commit, beacause you need to do dvc checkout or dvc pull 
dvc pull or dvc checkout
cat data.txt  ## see data is udpated with third commit
```  
</p>
</details> 
