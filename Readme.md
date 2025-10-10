Part 1: Refining Git History (10 Challenges)

  touch test{1..4}.md
  221  git add test1.md && git commit -m "chore: Create initial file"       
  222  git add test2.md && git commit -m "chore: Create another file"       
  223  git add test3.md && git commit -m "chore: Create third and fourth files"
  224  git add test4.md
  225  git commit --amend -m "chore: Create third and fourth files"
  226  git rebase -i HEAD~2
  227  git rebase -i HEAD~3
  228  git log --oneline
  229  git rebase -i --root
  230  git log --oneline
  231  git rebase -i HEAD~1
  232  git log --oneline
  233  git reset HEAD~1
  234  git add test3.md
  235  git commit -m "chore: Create third file"
  236  git add test4.md
  237  git commit -m "chore: Create fourth file"
  238  git log --oneline
  239  git rebase -i HEAD~2
  240  git log --oneline
  241  touch unwanted.txt
  242  git add unwanted.txt
  243  git commit -m "Unwanted commit"
  244  git rebase -i HEAD~1
  245  git log --oneline
  249  git log --oneline
  250  git checkout -b ft/branch
  251  echo "hello" > test5.md
  252  git add test5.md
  253  git commit -m "Implemented test 5"
  254  git checkout main
  255  git cherry-pick <hash-of-test5-commit>
  256  git log ft/branch --oneline
  257  git cherry-pick 6e596a9
  258  git log --oneline
  259  git log --oneline --graph --decorate --all
  260  git reflog
  261  git reset --hard HEAD@{2}
  262  history

  Part 3: Branching Basics

  git branch
  224  git checkout ft/branch
  225  git checkout main
  226  git stash
  227  git stash list
  228  git checkout ft/branch
  229  git merge main
  230  git branch
  231  git checkout ft/improved-branch-name
  232  git merge main
  233  git checkout main
