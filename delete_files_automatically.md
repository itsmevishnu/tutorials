## Delete Files from folders automatically in windows
Many times, it is headache to see all the unwanted files we downloaded last month in our download folder, List of draft file saved in the documents folder, cache files, ...
I am giving a short tip to handle these situtation effectively. 
We required two things., a small bash code and windows scheduler
#### Bash code to delete the files
Open your text editor( Notepad, Sublime or VS Code) and type following code
```
forfiles -p "C:\Users\Download" -s -m *.* /D -5 /C "cmd /c del @path"
```
This code will delete files older than 5 days(any type) from the given path(here C:\Users\Download)
You can change the parameters to change the options, like
```
forfiles -p "C:\Users\Download" -s -m *.docx* /D -30 /C "cmd /c del @path"
forfiles -p "C:\Users\Download" -s -m *.pdf* /D -30 /C "cmd /c del @path"
forfiles -p "C:\Users\Download" -s -m *.pdf* /D -0 /C "cmd /c del @path"
```
Save the file as a batch file. For that click on save, and then add '.bat' as the extension. Chnage text option to all files if you are using notepad.
Done. The code is ready.

#### Scheduling our application to run automatically
Windows has a system application called Task scheduler which will help to schedule automatic tasks. Type Task scheduler in windows search bar and enter.
1. Click on Action menu and select Create Task. 
2. It will open a window with 5 tabs.
3. First tab name is General. Enter the name and description about the scheduler. Give some descriptive name and description so that it will help later to understand the purpose of the scheduler.
4. Click on next tab - Triggers- Click on new trigger, and select the period you want to repeat your task. 
5. Next,  go to action tab, and click on New. Now enter the path of our bat file and OK.
6. The remaining tabs are more advanced options, which is not required for our current purpose.
Done!
