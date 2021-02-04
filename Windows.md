# Windows FAQ

**I get weird characters in my terminal when running `stack test` or some test output is not visible, what can I do?**

Windows does not have [UTF-8](https://en.wikipedia.org/wiki/UTF-8) enabled by default in command prompts. You can enable it temporarily for the duration of a session with `chcp 65001` or permanently with `reg add "HKLM\Software\Microsoft\Command Processor" /v Autorun /d "chcp 65001"` which will run the command every time you open a new command prompt. This also applies to Powershell.

**I get an error complaining about `<stderr> commitAndReleaseBuffer: invalid argument (invalid character)`**

Same issue and fix as above.
