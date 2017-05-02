## Introduction

The CS Handbook is a online reference guide for learning algorithms and data structures in a way that could be understood without a strong math background.

## Home page

![Home page](Mainscreen.png?raw=true "Main page")

## Contributing

All the articles are stored in /data as my flavour of Markdown and loaded into a databse by a script.
Everything in /book is generated by book.php which gets articles from the database.

To fix typos and other errors, make a Pull Request changing the appropriate file in /data. No other change
is necessary.

All contributors will be recognized.

Contributors who make many PR's will be given a free book.

## setup

```
curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer
composer install
```

Create config/local_config.ini:

```
env=production

sections[] = Getting Started
sections[] = Fundamentals
sections[] = Recursion
sections[] = Sorting
sections[] = Data Structures
sections[] = Graph Theory
sections[] = Searches
sections[] = Dynamic Programming
sections[] = Strings

[db]
host = localhost
user=root
password=YOURPASSWORD
database = algorithms
```

Import articles into mysql

```
cd scripts
php migrateData.php
```
