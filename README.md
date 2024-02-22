# Test signing

Signing using an ssh-key

## Tests
 * Signing using `git commit -S -m "xxx"` works
 * After setting `git config --global commit.gpgsign=true` Autosigning works when commiting from command line or `git gui` and probably vscode.
 * Verify modifing README.md via github does **NOT** sign as it doesn't have the private key.
