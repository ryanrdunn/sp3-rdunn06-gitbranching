echo "# sp3-rdunn06-gitbranching" >> README.md
git init
git add README.md
git commit -m "master-commit 0"
git branch -M master
git remote add origin git@github.com:ryanrdunn/sp3-rdunn06-gitbranching.git
git push -u origin master

-- Create bug fix branch
git branch bug-fix

-- Edit file
echo "#Master commit 1" >> README.md
git add README.md
git commit -m "Master commit 1"

-- Edit file
echo "#Master commit 2" >> README.md
git add README.md
git commit -m "Master commit 2"

-- Change to bug-fix
git checkout bug-fix

-- Edit file
echo "bug-fix commit 3" >> README.md
git add README.md
git commit -m "bug-fix commit 3"

-- Edit file
echo "bug-fix commit 4" >> README.md
git add README.md
git commit -m "bug-fix commit 4"

-- Create bug fix experimental branch
git branch bug-fix-experimental

-- Merge and Resolve conflicts "Manually resolve conflicts with commit 5"
git merge master

-- Edit file
echo "bug-fix commit 5" >> README.md
git add README.md
git commit -m "bug-fix commit 5"


-- Edit file
echo "bug-fix commit 6" >> README.md
git add README.md
git commit -m "bug-fix commit 6"

-- Change to bug-fix-experiemental
echo "bug-fix-experimental commit 7" >> README.md
git add README.md
git commit -m "bug-fix-experimental commit 7"

-- Change to bug-fix-experiemental
echo "bug-fix-experimental commit 8" >> README.md
git add README.md
git commit -m "bug-fix-experimental commit 8"

-- Change to bug-fix-experiemental
echo "bug-fix-experimental commit 9" >> README.md
git add README.md
git commit -m "bug-fix-experimental commit 9"


-- Change to master
git checkout master

-- Change to master
echo "master commit 10" >> README.md
git add README.md
git commit -m "master commit 10"

-- Change to bug-fix
git checkout bug-fix


-- Merge and Resolve conflicts "Manually resolve conflicts with commit 11"
git merge bug-fix-experimental

--Manual update README.md
echo "bug-fix commit 11" >> README.md
git add README.md
git commit -m "bug-fix commit 11"

-- Edit file
echo "bug-fix commit 12" >> README.md
git add README.md
git commit -m "bug-fix commit 12"


-- Change to master
git checkout master

-- Merge and Resolve conflicts "Manually resolve conflicts with commit 13"
git merge bug-fix

--Manual update README.md
echo "bug-fix commit 13" >> README.md
git add README.md
git commit -m "master commit 13"


--Manually add Commit graph and FILE.md
echo "Adding Commit graph and FILE.md commit 14" >> README.md
git add *
git commit -m "master commit 14"
