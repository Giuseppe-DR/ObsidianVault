To create a local repository, in a bash terminal

First create a folder using:
```bash
mkdir FolderName
cd FolderName
```

Create a new txt file:
```bash
touch chapter1.txt

```

Then init git
```bash
git init
```

Open the file in vs code with:
```bash
code chapter1.txt
```

Check what’s currently in your staging area, and add chapter1.txt:
```bash
git status
git add chapter1.txt
```

Commit your changes with:
```bash
git commit -m "Complete chapter1"

```

See what commits have been made with:
```bash
git log

```

Make a remote repo on github;
Move in the working directoy for the project you want to push.

```bash
git remote add origin https://github.com/Giuseppe-DR/Story.git
git branch -M main
git push -u origin main
```
