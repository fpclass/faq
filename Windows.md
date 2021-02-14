# Windows FAQ

Windows is a terrible platform for Computer Scientists to work on. This FAQ addresses common questions that arise from using Windows and recommendations for fixing them, but a much better solution in the long run is to switch to Linux or macOS.

### I get weird characters in my terminal when running `stack test` or some test output is not visible, what can I do?

Windows does not have [UTF-8](https://en.wikipedia.org/wiki/UTF-8) enabled by default in command prompts. You can enable it temporarily for the duration of a session with `chcp 65001` or permanently with `reg add "HKLM\Software\Microsoft\Command Processor" /v Autorun /d "chcp 65001"` which will run the command every time you open a new command prompt. This also applies to Powershell.

### I get an error complaining about `<stderr> commitAndReleaseBuffer: invalid argument (invalid character)`

Same issue and fix as above. This happens even if you are working on e.g. the DCS systems via a terminal client running on Windows.

### I get an error when running `stack test` mentioning that "Executable git not found on path: ...".

You need to [install git](https://git-scm.com/download/win) and reopen your terminal once it is installed. 

### I use OneDrive and occasionally I get random errors when running `stack` commands.

Do not work in folders controlled by OneDrive (or other similar systems, such as Dropbox). They acquire locks on your files which stops other programs from working correctly. Consider using a version control system (e.g. `git`) instead and make use of the GitHub Classroom repositories provided.

### Text I enter into the REPL gets messed up and nothing works correctly.

You have likely pressed Ctrl+C at some point which doesn't work properly in Haskell programs on Windows. Re-opening your terminal should fix the issue.
