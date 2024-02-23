# Test signing

Signing using an ssh-key

## Tests
 * Signing using `git commit -S -m "xxx"` works
 * After setting `git config --global commit.gpgsign=true` Autosigning works when commiting from command line or `git gui` and probably vscode.
 * Verify modifing README.md via browser signs commit using github's key. It can't sign with mine as it only has my public key!
![image](https://github.com/winksaville/test-ssh-git-commit-signing/assets/1024284/3f5691b8-5d4e-4f0c-a60d-b8bf8ecb0637)

 * Verify that modifying README.md on my laptop with where you can sign
   a key **without** adding the key to ssh-agent.
```
wink@fwlaptop 24-02-23T01:05:41.847Z:~/prgs/rust/myrepos/test-ssh-git-commit-signing (main)
$ git log -1 --show-signature 
commit 8cfc75fcd4c43b6dd2f5ddd48c447803f367945a (HEAD -> main)
Good "git" signature for * with ED25519 key SHA256:m4d1AYJSFVL79IMGP+9+91cNMKVUr/Co9VdaOzeujTw
Author: Wink Saville <wink@saville.com>
Date:   Thu Feb 22 17:05:04 2024 -0800

    doc: Update README.md
    
    Verifying we don't need the key added to ssh-agent.
wink@fwlaptop 24-02-23T01:06:21.073Z:~/prgs/rust/myrepos/test-ssh-git-commit-signing (main)
$ ssh-add -l
The agent has no identities.
wink@fwlaptop 24-02-23T01:06:48.108Z:~/prgs/rust/myrepos/test-ssh-git-commit-signing (main)
```
