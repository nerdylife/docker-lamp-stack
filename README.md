# Usage
With the following command the container start and build automaticly:
`docker-compose run -d`

If you made changes on apache, php or mysql config, you need to build
the speccified image, as example, with:
`docker-compose build php`

# Rights
if there are permission issues, try to set the folder and file permission inside the php container as follows:
`chown -R www-data:www-data /var/www/storage/`

In this example i needed the storage folder outside of the docroot and then
i needed to set new permissions.
