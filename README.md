# OnceInAWhile

Finding all HTML tags with a specific class in a source code of webPage and saving the entire line into a txt file
```
curl https://www.abcd.com | grep titles > articleTitles.txt
```
---

Finding out the name of the WI-FI connected to
```
/System/Library/PrivateFrameworks/Apple80211.framework/Versions/Current/Resources/airport -I | sed -e "s/^  *SSID: //p" -e d
```
---

Renaming files in a directory in sequential order
```
ls | cat -n | while read n f; do mv "$f" "$n.<extension>"; done
```
Source: http://stackoverflow.com/questions/3211595/renaming-files-in-a-folder-to-sequential-numbers

---

Playing a sound on terminal (say you want a done beep after a long task has completed)
```
afplay /System/Library/Sounds/Ping.aiff 
```
NOTE: More system sounds in the above directory

---

Re-implementation of ```git add -u``` command, to add only tracked files to the staging area
```
git status -uno | grep 'modified' | cut -c 14- | xargs git add
```

---

Deleting multiple git branches
```
git branch -d `git branch --list 'feature/project1*'`
```

Getting rid of new lines from a multi-line command in terminal and copying to back pasteboard
```
pbpaste | tr -d '\n' | pbcopy
```

