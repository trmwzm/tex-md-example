# LaTex
Repository with latex scripts

## Use LaTex formulas in github README.md
Python script [readme2tex](https://github.com/leegao/readme2tex) enables to compile formulas into svgs and embed them in your README.md

A useful trick to avoid polluting your repository is to build a specific branch to store the image files, and then add a git hook so the readme input is automatically compiled at each commit:
```
git branch svgs
python -m readme2tex --output README.md --branch svgs --user user --project project INPUT.md --add-git-hook
```

Then after each change in INPUT.md, you can commit the changes as such:
```
git add INPUT.md
git commit -a -m "updated readme"
git push --all origin
```

