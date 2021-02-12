# UploadR - PHP simple file upload interface

## Features

- Upload files in hidden folders and share by link
- Customise folder name
- Create link for others to upload files
- Username/password authentication
- Log incorrect credentials/self-upload links

## Requirements

- PHP 7 or above
- A folder writable for the user that PHP runs as (usally _www-data_)
- Optional, but recommended, `.htaccess` enabled

## Configuration

- Default username `admin` and password `admin`, please change immediately
- `$FOLDER_LOCATION` is the path of the writable folder for uploads (ex. `/var/www/upload-folder/`)
- `$URL_OF_FOLDER` is the public web address of the folder (ex. `https://example.com/upload-folder/`)
- `$URL_OF_UPLOADR` is the public web address of the file `uploadr.php` (ex. `https://example.com/uploadr.php`)
- `$LOG_LOCATION` is the path of the optional log file (or `FALSE` to disable logging). The file should be also writable for the user `www-data`
- `$USERS` is an array of 2-components array, where `user` is the username in plain text and `pwd` is the hashed version of the password for that user (the hash can be created from the interface itself, `Generate password hash` or with the PHP function `password_hash("<password text>",PASSWORD_DEFAULT)`
