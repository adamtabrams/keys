# About

Keys is a simple password management tool. It provides a wrapper and interface
for GPG, making it easy to store and access passwords.


# Setup

Install GPG and fzf.
* For MacOS: `brew install gpg fzf`

Create a GPG key.
* `gpg --full-generate-key`
* Make sure you give your key a good password!
* I configure my keys like this.
    * key kind*: RSA and RSA
    * key size: 4096
    * valid for: 1y

Clone this repo.
* `git clone https://github.com/adamtabrams/keys.git`

Add the executable to your path.
* Add the whole directory: `~/repos/keys:$PATH;`
* Copy into current path: `cp keys ~/.local/bin/`
* Link to it (my preference): `ln -s ~/repos/keys/keys ~/.local/bin/keys`


# Usage

Retrieve a key: `keys`
* lists your keys so you can select one
* attempts to unlock with key with GPG
* copies its password to your clipboad
* prints its username

Add a key: `keys add github`

Update a key: `keys update`
* allows you to change username or password

Remove a key: `keys remove` or `keys rm`


# Tips

* Keys can generate a password for you when adding or updating a key.

* GPG handles the passowrd prompts and can cache your password for a short time.
