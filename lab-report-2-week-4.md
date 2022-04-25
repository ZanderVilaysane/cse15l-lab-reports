# Lab Report 2, Week 4
## Author: Zander Vilaysane

### Code Change 1: Parenthesis Within a Link
### Screenshot of Code Change
![Parenthesis Within a Link][Code Changes SS1]
> Commits made by group member, Gabriel Castillo Gonzales

Click [*here*][test-file3.md] for the failure-inducing input, that being a link with parenthesis embedded
### Screenshot of Failure-inducing Input's Symptom
![CommandLine SS1][CommandLine SS1]
-  Note: The cmd line above showcases a OutOfMemory error due to retrieval of original parser file. Earlier testing shows different symptoms discussed below.

This markdown file contains a hyperlink with parenthesis syntax embedded within. This causes a bug where the parser's logic assumes that the link ends at the first end parenthesis it reads. The symptom originally had a return statement that would list the link but incompletely, stopping right before the closing parenthesis appeared in the link. To resolve this, we constructed an if condition to check if the closing parenthesis was the last index value of that line. If true, the parser would recognize that this is the full string of the link. 

---
### Code Change 2: Ending Markdown File w/ Empty New Line
### Screenshot of Code Change
![Empty New Line][Code Changes SS2]
> Commits made by group member, Jenny Quach

Click [*here*][test-file.md] to view the failure-inducing input, that being code with a new line at the end
### Screenshot of Failure-inducing Input's Symptom
![CommandLine SS2][CommandLine SS2]
This markdown file contains a valid hyperlink but the file itself ends with a empty new line. This causes a bug where the parser continues to read the file for links, assuming that they can be found in further lines. The symptom is a large runtime, eventually leading to a OutOfMemory error due to the program infintely running as the parser is continuing to search for possible lines of links. To resolve this, we constructed an if condition that checks if there is a new line `\n` at the current index. If true, the loop will break and stop, indicating that there is no more links beyond the last link of the file. 

---

### Code Change 3: No Links Found in Markdown File
### Screenshot of Code Change 
![No Links][Code Changes SS3]
Click [*here*][test-file2.md] to view the failure-inducing input, that being code with no links embedded (only text)
### Screenshot of Failure-inducing Input's Symptom
![CommandLine SS3][CommandLine SS3]
-  Note: The cmd line above showcases a OutOfMemory error due to retrieval of original parser file. Earlier testing shows different symptoms discussed below.

This markdown file contains text but holds no syntax for a hyperlink. This causes a bug where the parser does not recognize any index value of open/close brackets and parenthesis in the file, therefore these variables store a value of -1. The symptom originally had thrown a StringIndexOutOfBoundsException in earlier testing. To resolve this, we provided various if conditions to check if any of these brackets/parenthesis were missing (stored as -1) to determine if it was an empty link. If true, the parser would break the loop and return an empty ArrayList.

---
[Code Changes SS1]: https://user-images.githubusercontent.com/103156131/165001561-854a07ce-ae95-40a9-8dca-4ba1e786b6fa.JPG
[test-file3.md]: https://github.com/matchubi/markdown-parser-ZV/blob/main/test-file3.md?plain=1
[CommandLine SS1]: https://user-images.githubusercontent.com/103156131/165008280-412807de-ca82-4ce2-983e-964def6197e3.JPG
[Code Changes SS2]: https://user-images.githubusercontent.com/103156131/165002751-537c6e03-419a-4b27-88c8-75732fcd9427.JPG
[test-file.md]: https://github.com/matchubi/markdown-parser-ZV/blob/main/test-file.md?plain=1
[CommandLine SS2]: https://user-images.githubusercontent.com/103156131/165008256-380ecdef-c430-4691-a1c3-ec1f7a413b8f.JPG
[Code Changes SS3]: https://user-images.githubusercontent.com/103156131/165003328-b270a9af-e9c4-48da-a74f-38df53af6df2.JPG
[test-file2.md]: https://github.com/matchubi/markdown-parser-ZV/blob/main/test-file2.md?plain=1
[CommandLine SS3]: https://user-images.githubusercontent.com/103156131/165008203-8e9c41b8-f5e8-4272-a566-44a3a6376135.JPG

