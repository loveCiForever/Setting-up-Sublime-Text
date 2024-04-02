# Installation-guide-of-Sublime-Text 4
Installation guide of Sublime Text 4. Also, i will introduce a way to crack it for anyone who wants. 

## Install Sublime Text 4
* Download Sublime Text 4 here: https://www.sublimetext.com/3 . Choose the approriate version with your computer's system

## Setup environment GCC/G++ for Windows
* Follow this guy on Youtube: https://www.youtube.com/watch?v=8CNRX1Bk5sY

## Add new Build System file for C++ in SubLime Text 4
* Step 1: Open ST4, look at the menu bar (on the top) -> [Tools]  -> [Build system] -> [New Build system]                                                                          * Step 2: Copy the code below and save as "myC.sublime-build"
  
	    {
	        "encoding": "utf-8",
	        "working_dir": "$file_path",
	        "shell_cmd": "gcc -Wall -std=c++11 \"${file}\" -o \"${file_path}/${file_base_name}\"",
	        "file_regex": "^(..[^:]*):([0-9]+):?([0-9]+)?:? (.*)$",
	        "selector": "source.c",
	    
	        "variants":
	        [
	            {   
	                "name": "Run",
	                "shell_cmd": "gcc -Wall -std=c89 \"${file}\" -o \"${file_base_name}\" && start cmd /c \"\"${file_path}/${file_base_name}\" & echo. &echo ------------------------------ & echo Quang Huy Handsome had successfully compiled from LTP's compiler & pause\""
	            }
	        ]
	    }
        
* Step 3: Write some program and save it with extension ".cpp" (E.g.: Hello_World.cpp)                                                                                             * Step 5: In the first time, Press [Ctrl] + [Shift] + [B] at the same time. Next time just press [Ctrl] + [B] to compile and run your program

## Other way to compile and run your program
* Step 1: Open Command Prompt, WindowsPowerShell or Cygwin64 (to install Cygwin64, follow this guy: https://www.youtube.com/watch?v=nidNLiNUrQU)
* Step 2: Use the comman "g++ -o yourOutputFileName yourProgramName.cpp" (E.g.: g++ -o helloworld helloworld.cpp)
* Step 3: Execute it with "./helloworld" 
