# Installation guide of Sublime Text 4

## Install Sublime Text 4
* Download the approriate version with your computer's systemSublime Text 4 [here](https://www.sublimetext.com/download)

## Setup GCC/G++ environment for Windows
* Step 1: Download MinGW W64 [here](https://sourceforge.net/projects/mingw/)
* Step 2: Run mingw-get-setup.exe as administrator and Click on [Install]
* Step 3: Mark all the packages for installation
* Step 4: Click on the Apply Changes option under the Installation tab as shown below:

## Add new Build System file for C++ in SubLime Text 4
* Step 1: Open ST4, look at the menu bar (on the top) -> [Tools]  -> [Build system] -> [New Build system]
* Step 2: Copy the code below and save as "myC.sublime-build"
  
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
        
* Step 3: Write some program and save it with extension ".cpp" (E.g.: Hello_World.cpp)
* Step 5: In the first time, Press [Ctrl] + [Shift] + [B] at the same time. Next time just press [Ctrl] + [B] to compile and run your program

## Run and Compile a programm by Command Prompt.
* Step 1: Open Command Prompt, WindowsPowerShell.
* Step 2: Use the comman "g++ -o yourProgramName.cpp yourOutputFileName.exe" (E.g.: g++ -o test.cpp test.exe)
* Step 3: Execute it with "test.exe"
  ![image](https://github.com/loveCiForever/Setting-up-Sublime-Text-for-Competitive-Progaming-C-/assets/107240800/aace8fd1-7af5-43ed-ab3f-bf79f85d4805)



## How to activate Sublime Text 4
* Follow this repo: https://gist.github.com/skoqaq/3f3e8f28e23c881143cef9cf49d821ff#gistcomment-4824279
