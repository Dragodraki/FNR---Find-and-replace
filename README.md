# FindAndReplace
Find and replace content in files, reliable (stable), no matter the encoding, nor their size, nor whether the operation was successful or not.
(Release Date: 15.04.2024, Publisher: ZZZProjects & Dragodraki alias Dreamland, as fork this is a special version with some enhancements)
<br/>

[<img src="https://user-images.githubusercontent.com/76787321/197257488-1b7aa8e9-9b6f-4600-949e-8ff477cb4bf4.png" width="23%"></img>](https://github.com/Dragodraki/BringExeToFront/releases/latest/download/BringExeToFront.exe)
<br/>

-------------------------------
HOW IT WORKS TECHNICALLY
-------------------------------
The tool is written in C#, a standard WinForm application is used. ZZZProjects put very much effort into the technique of filtering and data processing. All you need to do is enter the folder path to your target file(s), the file name and the mask (what you look for and what it should be replaced with). I am not very familiar with the detailed work of regex and complicated binary comparisons, but these are available too. The GUI even offers a button for generating the whole options as one single command-line.
Thats one of the funniest things: Tools having a GUI but a (silent) command-line interface at the same time, need a WinForm. When entering parameter/command-line options, the WinForm will be started too, but immediately hidden so the user does not even notice. This way, there isn't any black console window blinking for a seccond and then disappear, but completely invisible. A normal double-clicking on the executable instead will open the GUI.

![basic-usage-1](https://github.com/Dragodraki/FNR---Find-and-replace/assets/76787321/8b8d9b48-f4af-4c0b-8255-d77bcc70af97)

-------------------------------
LICENSE (OPEN-SOURCE)
-------------------------------
Permissions:
+ Private and Commcercial usage is allowed as long you don't demand money for it ;)
+ Forks are welcome, but they have to kept free of charge ;)
+ Free Distribution to friends or strangers is allowed, even wanted ;)

Limitations:
- Use the app at your own risk!
- Don't sell it as product as the app is originally developed by ZZZProjects!
- Don't abuse it for malicious purposes!


-------------------------------
USAGE
-------------------------------
You can use the GUI mode by open with no parameter or the command-line interface like cmd, powershell, any other console or an automated call from script/program for automatic (batch) processing.

Syntax usage:  
- fnr.exe [-Parameter]<br/>

Parameters:  
--cl	Required to run on command line.
--find	Required. Text to find.
--replace	Replacement text. If not specified only find operation is performed.
--useRegEx	Use regular expressions in ‘find’ parameter.
--useEscapeChars	Use escape chars like ‘\n’ in ‘find’ and ‘replace’ parameters.
--caseSensitive	Case Sensitive.
--dir	Required. Directory path.
--includeSubDirectories	Include files in SubDirectories.
--fileMask	Required. File mask or multiple file masks separated by comma.
--excludeFileMask	File masks to exclude. If multiple - separate by comma
--help	Dispaly help screen.
--showEncoding	Displays detected encoding for each file with matches.
--silent	Supress the command window output.
--logFile	Path to log file where to save command output.
--skipBinaryFileDetection	Ignore detection of binary files.
--alwaysUseEncoding	Skip encoding detection and always use specified encoding.
--defaultEncodingIfNotDetected	If encoding is not detected in some very rare cases, use this one.
--includeFilesWithoutMatches	Include files without matches in results.
--setErrorLevelIfAnyFileErrors	Return ErrorLevel 2 if any files have read/write errors.
--cl	Required to run on command line.

Examples:  
- fnr.exe --cl --dir "C:\temp\myfolder" --fileMask "myfile.txt" --find "StringToSearch=123" --replace "StringToReplace=888"
This will target "C:\temp\myfolder\myfile.txt" only and replace the string "StringToSearch=123" with "StringToReplace=888" (both without quotation marks of course).<br/>

For detailed explanation look at this site: http://findandreplace.io/overview
<br/>
If the site will be down far in the future, search the url with archive.org :)
