# NGINX helper functions

This repo contains several scripts to help configure NGINX. It requires to have NGINX already configured to use `sites-available` & `sites-enabled`. 


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
