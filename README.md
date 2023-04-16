# NGINX helper functions

This repo contains several scripts to help configure NGINX. It requires to have NGINX already configured to use `sites-available` & `sites-enabled`. 

## Installation

### Quick way

This downloads the scripts, and tries to install it via your bash_profile.

`if [ ! -d ~/bin ]; then mkdir ~/bin; echo "export PATH=\$PATH:~/bin" >> ~/.bash_profile; fi && cd ~ && git clone https://github.com/JeffreyArts/nginx-helper-functions.git && cp nginx-helper-functions/* ~/bin/ && chmod +x ~/bin/* && source ~/.bash_profile`

If this does not work, please check if the line `PATH=\$PATH:~/bin` is located in your `~/.bash_profile` (and add it if not). For more debugging check de detailed instructions below.

### Detailed

1. Clone the repository to the server the command `git clone https://github.com/JeffreyArts/nginx-helper-functions.git`.

2. Navigate to the repository directory using the command `cd nginx-helper-functions`.

3. Copy the scripts to the `~/bin` directory using the command `cp * ~/bin/` (create ~/bin with `mkdir ~/bin` if it does not exist already)

4. Make the scripts executable using the command `chmod +x ~/bin/*`.

5. Open your shell profile file using the command `nano ~/.bash_profile` (if you're using bash) or `nano ~/.zshrc` (if you're using zsh).

6. Add the following line to the file: `export PATH=$PATH:~/bin`.

7. Save the changes and close the file.

8. Reload your shell profile using the command `source ~/.bash_profile` (if you're using bash) or `source ~/.zshrc` (if you're using zsh).

Now, the `add_site`, `disable_site`, and `create_static_site` scripts should be available for use from any directory on your machine.


## How to use
```
add_site <site>
```
This will enable a website, <site> should refer to the filename of the website as it is added to `sites-enabled`

```
  add_site <site>
  ```
This will disable a website, <site> should refer to the filename of the website as it is added to `sites-enabled`

```
  create_static_site <site>
```
This will create a website in the `sites-available` directory with the filename <site>. It will also prompt you where the location of the static website (/var/www/(...)) is located
