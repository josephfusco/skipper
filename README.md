<p align="center"><img width="300" src="https://user-images.githubusercontent.com/6676674/36431060-a04a276a-1624-11e8-9547-73937d54b0ff.png" alt="skipper"></p>


## Introduction

Skipper is a WordPress site setup script for [Laravel Valet](https://github.com/laravel/valet).

## Usage

For usage information:
```
skipper --help
```

### Site Creation

The skipper command should only be ran within the parked valet directory.

```
skipper mysite
```

Currently, the above command will do the following:

+ Create a new directory called `mysite`
+ Download & install the latest version of WordPress, including the database. (database name will be `valetwp_mysite`)
+ Remove default plugins (Akismet & Hello Dolly)
+ Remove default themes except Twenty Seventeen
+ Set front page as "Home"
+ Set posts page as "Blog"
+ Add "Home" & "Blog" to primary menu
+ Discourage search engines
+ Change permalinks to use `/%postname%/`
+ Install & activate plugin "[Disable Comments](https://github.com/solarissmoke/disable-comments)" & set option to disable all comments.
+ Install & activate plugin "[WP Self Destruct](https://github.com/josephfusco/wp-self-destruct)"

Once done, the site will open in your default browser and automatically log you in as the admin user.

### Divi

Skipper supports quick site setup using the [Divi theme](https://www.elegantthemes.com/gallery/divi/).

```
skipper mysite --divi
```

The `--divi` flag will install and activate the Divi theme. "Home" & "Blog" pages will be assigned to the theme's main navigation menu location.

**Note:** You must provide your Elegant Themes username and API key to use this feature. These credentials will only be stored locally in `~/.skipper/et.json`.
