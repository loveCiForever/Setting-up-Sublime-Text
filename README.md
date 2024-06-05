# Installation guide of Sublime Text 4

## Install Sublime Text 4
* Download the approriate version with your computer's systemSublime Text 4 [here](https://www.sublimetext.com/download)

## Setup GCC/G++ environment for Windows
* Step 1: Download MinGW W64 [here](https://sourceforge.net/projects/mingw/)
  
* Step 2: Run mingw-get-setup.exe as administrator and Click on [Install]
* Step 3: Mark all the packages for installation
* Step 4: Click on the [Apply Changes] option under the Installation tab.

## Add new Build System file for C++ in SubLime Text 4
* Step 1: Open Sublime Text, look at the menu bar (on the top) -> [Tools]  -> [Build system] -> [New Build system]
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
				"shell_cmd": "gcc -Wall -std=c89 \"${file}\"
				-o \"${file_base_name}\"
				&& start cmd /c \"\"${file_path}/${file_base_name}\"
				& echo. &echo ------------------------------ & echo Quang Huy Handsome had successfully compiled from LTP's compiler & pause\""
	            }
	        ]
	    }
        
* Step 3: Write your first program and save it with extension ".cpp" (E.g.: Hello_World.cpp)
* Step 4: In the Tool Tab, Click on [Build System] -> [myC]
* Step 5: In the first time, Press [Ctrl] + [Shift] + [B] at the same time. Next time just press [Ctrl] + [B] to compile and run your program

## Run and Compile a programm by Command Prompt.
* Step 1: Open Command Prompt, WindowsPowerShell.
* Step 2: Use the comman "g++ -o yourProgramName.cpp yourOutputFileName.exe" (E.g.: g++ -o test.cpp test.exe)
* Step 3: Execute it with "test.exe"
  
  ![image](https://github.com/loveCiForever/Setting-up-Sublime-Text-for-Competitive-Progaming-C-/assets/107240800/aace8fd1-7af5-43ed-ab3f-bf79f85d4805)

## Set up Sublime Text for Competitve Programming
* Step 1: Create 3 file: sourceCode.cpp, inputf.in, outputf.out
  
  ![image](https://github.com/loveCiForever/Setting-up-Sublime-Text-for-Competitive-Progaming-C-/assets/107240800/80d1d66c-1c20-4b36-8993-73200a5c14de)
  
* Step 2: Open Sublime Text.
* Step 3: In the View Tab, Click on [Layout] -> [Columns: 3] or [Alt] + [Shift] + [3]
* Step 4: In the View Tab, Click on [Group] -> [Max groups: 2]. After those step, we will have this layout.
  
  ![image](https://github.com/loveCiForever/Setting-up-Sublime-Text-for-Competitive-Progaming-C-/assets/107240800/dd55a742-2e2a-4e85-b421-d9a21a5f08ed)
  
* Step 5: Save this build file system as "CPP_CP.sublime-build"
  
		{
			    "cmd": ["g++.exe", "-std=c++17", "${file}",
			            "-o", "${file_base_name}.exe",
			            "&&", "${file_base_name}.exe<inputf.in>outputf.out"],
			    "shell":true,
			    "working_dir":"$file_path",
			    "selector":"source.cpp"
		}
  
* Step 6: In the Tool Tab, Click on [Build System] -> [CPP_CP]
* Step 7: In the first time, Press [Ctrl] + [Shift] + [B] at the same time. Next time just press [Ctrl] + [B] to compile and run your program
    
## How to activate Sublime Text 4
* Follow this repository: https://gist.github.com/skoqaq/3f3e8f28e23c881143cef9cf49d821ff#gistcomment-4824279
