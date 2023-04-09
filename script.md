```
# homebrew
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

$ brew install --cask iterm2
$ brew install zsh
$ brew install git
$ brew install lighttpd
brew install selfcontrol
brew install --cask sublime-text
brew install mysql
brew install bat
 brew install curl
 brew install --cask postman



```

set up git signing
Install GPG if it's not already installed on your system. On a Mac, you can install it using Homebrew with the command brew install gnupg.

Generate a GPG key pair with the command gpg --full-generate-key. Follow the prompts to set up the key pair, including creating a passphrase to protect your private key. You may want to choose the RSA key type and 4096 bits for better security.

List your GPG keys with the command gpg --list-secret-keys --keyid-format LONG. Find the ID of the key you just generated, which will be a 16-digit hexadecimal string starting with sec.

Configure Git to use your GPG key for signing commits with the command git config --global user.signingkey <GPG key ID>.

Set Git to sign all commits automatically with the command git config --global commit.gpgsign true.
Optionally, configure your Git commit message template to include a line for signing the commit. Create a file called .gitmessage.txt in your home directory and add the following lines to it:


# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
# Your commit message should include a brief summary of the changes
# followed by a detailed explanation of the changes, if necessary.
#
# Signed-off-by: Your Name <youremail@example.com>
Configure Git to use your message template with the command git config --global commit.template ~/.gitmessage.txt.