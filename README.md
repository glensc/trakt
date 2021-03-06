# Trakt.tv import/export tools

## Purpose

 * Import Movies or TVShows IDs from CSV file format into Trakt.tv.

 * Export Movies or TVShows IDs from Trakt.tv list into CSV file format.

 * Create trakt.tv custom list from TDMB discover with filter.

## Requirements

You must use Python 2.7.x.

##### On Ubuntu/Debian Linux system

Ensure you are running Python 2.7
```
        $ python -V
Python 2.7.9
```

Install need module dependencies

        $ apt-get install python-dateutil python-simplejson python-requests python-openssl jq

##### On Windows system

 Download the installer: https://www.python.org/ftp/python/2.7.16/python-2.7.16.msi

 Ensure you are running Python 2.7
```
        C:\Python27>python.exe -V
Python 2.7.16
```

 Install need module dependencies

        C:\Python2.7\Scripts\easy_install-2.7.exe simplejson requests

## Usage

* Create an [Trakt.tv application](https://trakt.tv/oauth/applications) to have your own ``client_id`` and ``client_secret``, https://trakt.tv/oauth/applications.
You only need to fill up the ``Name`` with a ``Description`` and ``Redirect uri`` to whatever (i.e. https://zapp.com, it is not being used), leave the rest empty and click on ``SAVE APP``.

* Run the script to create a default config file ``config.ini``

        $ python export_trakt.py

* Edit the config file ``config.ini`` and specify the ``client_id`` and ``client_secret`` as well as any other settings appropriate to your enviromenent, eg: URL, proxy, etc...
Refer to ``Configuration details`` section for more information.

        $ vim config.ini

* Run the script to authenticate against Trakt.tv API using the PIN method and it will generate you an ``oauth_token``.
You will be prompted to open a link into a browser and paste the pincode back to the script. 
Make sure you save the generated ``oauth_token`` into the config file ``config.ini`` for later use.

        $ python export_trakt.py


## Import 

[Import CSV into trakt.tv](https://github.com/xbgmsharp/trakt/blob/master/import.md)

## Export

[Export data from trakt.tv into CSV](https://github.com/xbgmsharp/trakt/blob/master/export.md)

## Sync

[Create trakt.tv list from TDMB discover with filter](https://github.com/xbgmsharp/trakt/blob/master/sync.md)

## Export data from Kodi

Export Movies or TVShows IDs from Kodi into CSV file format.
[Export data from Kodi](https://github.com/xbgmsharp/trakt/blob/master/KODI.md)

## Export data from CouchPotato

Export Movies IDs from CouchPotato into CSV file format.
[Export data from CouchPotato](https://github.com/xbgmsharp/trakt/blob/master/CouchPotato.md)

## Support

To get support, please create new [issue](https://github.com/xbgmsharp/trakt/issues)

## Licence

This script is free software:  you can redistribute it and/or  modify  it under  the  terms  of the  GNU  General  Public License  as published by the Free Software Foundation.

This program is distributed in the hope  that it will be  useful, but WITHOUT ANY WARRANTY; without even the  implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

See <http://www.gnu.org/licenses/gpl.html>.
