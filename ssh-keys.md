### Generating and Adding Your SSH Key

You will want to add your SSH key to both GitLab (vanderbilt.bootcampcontent.com) and GitHub (github.com).

#### MacOS

1. Open Terminal
2. Type `ssh-keygen -t rsa -b 4096 -C "<YOUREMAIL@YOURMAIL.COM"` and hit return on each of the items, no need to change the file or add a passphrase
3. Type `eval "$(ssh-agent -s)"` and hit return
4. Type `ssh-add -K ~/.ssh/id_rsa` and hit return
5. Type `pbcopy < ~/.ssh/id_rsa.pub` (this copies your key)
6. Open up GitLab, head over to Settings > SSH Keys and then add new key, hit CMD-V to paste the key and then hit save.

#### Windows

1. Open Terminal
2. Type `ssh-keygen -t rsa -b 4096 -C "<YOUREMAIL@YOURMAIL.COM"` and hit return on each of the items, no need to change the file or add a passphrase
3. Type `eval "$(ssh-agent -s)"` and hit return
4. Type `ssh-add ~/.ssh/id_rsa` and hit return
5. Type `clip < ~/.ssh/id_rsa.pub` (this copies your key). If you're unable to use `clip`, you might try `cat ~/.ssh/id_rsa.pub` to copy your key
6. Open up GitLab, head over to Settings > SSH Keys and then add new key, hit CMD-V to paste the key and then hit save.
