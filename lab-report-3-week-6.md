# Lab Report 3 - Week 6
## Author: Zander Vilaysane

## Streamlining ssh Configuration
### Shown below is my `.ssh/config` file in VScode format: 
![.ssh/configSS][configFile]
### An `ssh` command was used but please note: I had trouble creating an alias where a password was not needed but an attempt was still made and documented below:
![sshLoginSS][sshLogin]
### An `scp` command that copies a file into my account is shown below. For this demonstration, we will be adding an example file called `scpTester.md` 
![scpcmdFileSS][scpcmd]

## Setup Github Access from ieng6
### The GitHub key is showcased below via GitHub browser access:
![pubSS][pubKey]
### Both the public `.pub` and private keys can be seen below in my user directory on the side panel:
![user side][keys]
### Running `git` commands with the intentions of committing and pushing were made and documented below:
![gitCommands][gitcmd]
- Click [HERE][commitLink] to view the commits that were made

## Copy whole directories with `scp -r`
### Using `scp -r` with the parameters: `.` (for all content) and `ieng6:~\markdown-parser` (for directory) we are able to copy the entirety of the directory into our `ieng6` account as shown below: 
![scp-rSS][scp-rcopy]
### After copying the directory, we can try to run the JUnit testers found in the markdown-parser repo: 
![testersSS][testers]
> The JUnit testers do run, but as shown above, it shows that it does have a failure (likely from not calling test-file.md, however there was an issue where the bug claimed that there was no test-file.class found)

### With the use of `;` we are able to run multiple commands in one line. Shown below is reiterating the same process as above with `scp-r` and the Junit testers running:
![onelinecmdSS][onelinecmd]
> The attempt is shown above but because of the password access, permission is denied.

---
[configFile]: https://user-images.githubusercontent.com/103156131/167322618-7c82dae8-d07f-4777-969d-514649d6ebc1.JPG
[sshLogin]: https://user-images.githubusercontent.com/103156131/167322798-18d6a97a-d5f5-471d-9a9d-e231a1222907.JPG
[scpcmd]: https://user-images.githubusercontent.com/103156131/167322824-d08a7361-4863-4ce4-aba5-23c49037f94e.JPG
[pubKey]: https://user-images.githubusercontent.com/103156131/167322679-3428fc86-d48c-4414-a971-75f5aa598229.JPG
[keys]: https://user-images.githubusercontent.com/103156131/167322618-7c82dae8-d07f-4777-969d-514649d6ebc1.JPG
[gitcmd]: https://user-images.githubusercontent.com/103156131/167322763-3c467a73-f9ac-4c4f-b00d-6c7d60cf1cd1.JPG
[commitLink]: https://github.com/matchubi/skill-demo/commit/2107bc85ce103611b669dbc43b28f343d5ed4a86
[scp-rcopy]: https://user-images.githubusercontent.com/103156131/167322719-2a8c534f-cc2d-48f6-b308-350a5384f5e2.JPG
[testers]: https://user-images.githubusercontent.com/103156131/167322700-b642de1c-5499-4311-bbed-c29c5101375e.JPG
[onelinecmd]: https://user-images.githubusercontent.com/103156131/167322647-83e5132f-944a-492d-86b1-3a8fc9678820.JPG
