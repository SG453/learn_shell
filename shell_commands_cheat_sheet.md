# Linux Bash Shell Cheat Sheet 
_______________________

## Basic Terminal Shortcuts 
- CTRL  L  = Clear the terminal 
- CTRL  D =  Logout 
- SHIFT  Page Up/Down = Go up/down the terminal 
- CTRL  A = Cursor to start of line 
- CTRL  E = Cursor the end of line 
- CTRL  U = Delete left of the cursor 
- CTRL  K = Delete right of the cursor 
- CTRL  W = Delete word on the left  
- CTRL  Y = Paste (after CTRL U,K or W) 
- TAB = auto completion of file or command 
- CTRL R = reverse search history 
- !! = repeat last command 
- CTRL Z = stops the current command (resume with fg in foreground or bg in background) 

________________

## Basic Terminal Navigation
- ls -a = list all files and folders 
- ls \<folderName> = list files in folder 
- ls -lh = Detailed list, Human readable 
- ls -l *.jpg = list jpeg files only 
- ls -lh <fileName> = Result for file only 
- cd \<folderName> = change directory if folder name has spaces use “ “ 
- cd / = go to root 
- cd .. = go up one folder, tip: ../../../
- du -h: Disk usage of folders, human readable
- du -ah: “ “ “ files & folders, Human readable 
- du -sh: only show disc usage of folders 
- pwd = print working directory 
- man \<command> = shows manual (RTFM) 
  
______________
  
## Basic file manipulation

- cat \<fileName> = show content of file (less, more) 
- head = from the top -n \<#oflines> \<fileName> 
- tail = from the bottom -n \<#oflines> \<fileName> 
- mkdir = create new folder 
- mkdir myStuff .. 
- mkdir myStuff/pictures/ ..
- cp image.jpg newimage.jpg  = copy and rename a file
- cp image.jpg <folderName>/ = copy to folder 
- cp image.jpg folder/sameImageNewName.jpg 
- cp -R stuff otherStuff = copy and rename a folder 
- cp *.txt stuff/ = copy all of *<file type> to folder 
- mv file.txt Documents/ = move file to a folder 
- mv \<folderName> \<folderName2> = move folder in folder 
- mv filename.txt filename2.txt = rename file 
- mv \<fileName> stuff/newfileName 
- mv \<folderName>/ .. = move folder up in hierarchy 
- rm \<fileName> .. = delete file (s) 
- rm -i \<fileName> .. = ask for confirmation each file  
- rm -f \<fileName> = force deletion of a file 
- rm -r \<foldername>/ = delete folder touch \<fileName> = create or update a file 
- ln file1 file2 = physical link 
- ln -s file1 file2 = symbolic link 
  
______________________
## Researching Files

- The slow method (sometimes very slow):   
- locate <text> = search the content of all the files 
- locate <fileName> = search for a file 
- sudo updatedb = update database of files 
- find = the best file search tool(fast) 
- find -name “<fileName>” 
- find -name “text” = search for files who start with the word text 
- find -name “*text” = “ “ “ “ end

_______________________________
  
## Advanced Search: 
- Search from file Size (in ~)  
  1. find ~ -size +10M = search files bigger than.. (M,K,G) 
- Search from last access 
  1. find -name “<filetype>” -atime -5 
  ('-' = less than, '+' = more than and nothing = exactly) 
- Search only files or directory’s 
  1. find -type d --> ex: find /var/log -name "syslog" -type d 
  2. find -type f = files 
- More info: man find, man locate 

