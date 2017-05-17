# Enhancing Accessibility with Engaging Filters
#### Epicodus Capstone Project
## By Benjamin T. Seaver
This project intends to enhance the user's ability to cover long lists of short text abstracts such as tweets.  

Instead of requiring the user to sequentially read through a long list and fight to maintain concentration, she may instead say:

* Show me the tweets with the highest likes or shares.

* Show me the authors of the tweets in this list.  Show me the tweets of this author.  

* Show me the locations of tweets.  Show me the tweets at this location.  

* Show me the tweets with words having the highest scoring scrabble scores.  

* Show me the tweets I have not seen so far.  

The idea is that by enabling her to read portions of the list via a variety of engaging filters, she may manage to more thoroughly cover the available content and find more of the interesting content.

### Minimum Viable Product (MVP)
* Retrieve a list of a hundred tweets.
* Optionally Filter tweets to those not yet seen since last retrieving.
* Also optionally filter by:
  * Author
  * Likes
  * Shares
  * Retweets
  * Location of Author
  * High Scrabble Score words

### Intended Tools and Frameworks:
* Drupal with Twitter and Views modules
* Possible Custom Module (not sure yet if needed)
* JavaScript for Filtering

### After reaching MVP, if time allows, I may work on:
* Extend search criteria to other values derived from the tweets - such as tags, mentions, has images etc.
* Enable searching hundreds of tweets (not just one hundred).
* Extend retrieval of tweets to different criteria such as a search expression vs a user's timeline.
* Since the Twitter API is rate limited by the owner of the Twitter account, seek to retrieve data based upon the user's Twitter account so that multiple users can use the facility without immediately running into rate limiting.

### Requires previous installation of:
  * Git (https://git-scm.com/downloads)
  * MAMP (https://www.mamp.info/) to host the Website and MySQL Database

### Utilizes:
  * Drupal 7.54 (https://www.drupal.org/)

### Installation Notes From GitHub:
  * git clone this repo on your desktop
  * This cloned folder is the project or site folder
  * The folder may be renamed at this point to your preference or convenience
  * Database, database user and all passwords are `drupal`.  Site admin name is `Benjamin`.
  * Using MAMP by opening `localhost:8888/phpmyadmin/`, first create a new database named `d7-twitter` with collation `utf8_general_ci`.
  * Create a DB user with all privileges (except grant) with name and password of `drupal`
  * Site database is stored in sites/db-backup/ and needs to be imported into the `d7-twitter` database.
  * Set MAMP's Host Document Root folder to site folder, restart servers
  * Launch site by opening `localhost:8888/`

### Summary of Steps Used to Create a Drupal Site:
* Copy downloaded Drupal core to the Desktop (for convenience)
* Rename the Drupal core folder to indicate the name of the project
* The following commands apply from the root of the project folder:
* Rename (to effectively remove) .gitignore
* The following may be needed in access controlled environments:
  * $ `chmod -R a+w sites/default`
  * Copy `project/sites/default/default.settings.php` to `project/sites/default/settings.php`
* Set MAMP's Host Document Root folder to project folder, restart servers
* Open SQL page `localhost:8888/phpmyadmin/`
* Create database with collation `utf8_general_ci`
* Create admin user for Drupal site's internal use
* Open `localhost:8888/` for new Drupal site
* Setup: Standard, English, Database, host and port 127.0.0.1 and 8889
* Initial Site name, email, admin user, country, time zone and turn off e-mail notices for demonstration purposes
* Verify initial site is working
* Create a README.md file in the project root
* Commit the README.md
* Commit initial Drupal files and database backup
* Iteratively, add features to site and commit

### Incremental and Final Save of Site Database
* Export MAMP hosted database specifying:
  * Custom, SQL, All Tables (structure and data)
  * Save output to File, Compression: zipped
  * Add option: create database
  * Add option: drop table
* Save zip file to sites/db-backup/ (replacing previous copy if any)
* Add and Commit this file to the git repository

### Contribs Used
* Twitter 7.x-5.11
* OAuth 7.x-3.4
* views 7.x-3.16
* ctools 7.x-1.12
* entity 7.x-1.8
* Token 7.x-1.8 

## Copyright (c)
* 2017 Benjamin T. Seaver

## Known Bugs
* No known bugs

## Support and contact details
* None

## License
* MIT

##### End of File
