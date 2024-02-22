# Test signing

Signing using an ssh-key

## Tests
 * Signing using `git commit -S -m "xxx"` works
 * After setting `git config --global commit.gpgsign=true` Autosigning works when commiting from command line or `git gui` and probably vscode.
 * Verify modifing README.md via browser signs commit using github's key. It can't sign with mine as it only has my public key!
![image](https://github.com/winksaville/test-ssh-git-commit-signing/assets/1024284/3f5691b8-5d4e-4f0c-a60d-b8bf8ecb0637)
