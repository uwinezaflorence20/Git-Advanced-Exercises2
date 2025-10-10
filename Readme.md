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

  git stash pop
  241  git stash list
  242  git stash
  243  git stash list
  244  git stash apply
  245  git stash list
  246  git stash pop
  247  git stash
  248  history

  git checkout ft/branch
  254  git merge main
  255  git checkout main
  256  git merge ft/branch
  257  git checkout ft/branch
  258  git nmerge main
  259  git merge main
  260  git branch
  261  git checkout main
  262  echo "Original line" > example.txt
  263  git add example.txt
  264  git commit -m "Add example.txt with original line"
  265  echo "This is the main branch change" > example.txt
  266  git add example.txt
  267  git commit -m "Change example.txt in main"
  268  git checkout ft/branch
  269  echo "This is the ft/branch change" > example.txt
  270  git add example.txt
  271  git commit -m "change example.txt in ft/branch"
  272  git checkout main
  273  git merge ft/branch
  274  git add example.txt
  275  git commit -m "resolve comflict between main and ft/branch"
  git config --global merge.tool vscode
  286  git config --global mergetool.vscode.cmd "code --wait $MERGED"
  287  git add conflict.txt
  288  git commit -m "added the conflict"
  289  git checkout ft/branch
  290  git checkout main
  291  git add conflict.txt
  292  git commit -m "added the conflict"
  293  git checkout ft/branch
  294  git merge main
  295  git add conflict.txt
  296  git commit -m "added the conflict"
  297  git checkout main
  298  git checkout main
  299  echo "Original line" > examples.txt
  300  git add examples.txt
  301  git commit -m "Add example.txt with original line"
  302  echo "This is the main branch change" > example.txt
  303  git add example.txt
  304  git commit -m "Change example.txt in main"
  305  git checkout ft/branch
  306  echo "This is the ft/branch change" > example.txt
  307  git add example.txt
  308  git commit -m "Change example.txt in ft/branch"
  309  git checkout main
  310  git merge ft/branch
  311  git config --global merge.tool vscode
  312  git config --global mergetool.vscode.cmd "code --wait $MERGED"
  313  git merge ft/branch
  314  git mergetool
  315  git merge ft/branch
  316  git add example.txt
  317  git merge ft/branch
  318  git commit -m "saved the changes"
  319  git merge ft/branch
