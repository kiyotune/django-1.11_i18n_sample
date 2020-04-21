# i18n sample by Django 1.11
## How to use

```
$ git clone https://github.com/kiyotune/django-1.11_i18n_sample
$ cd django-1.11_i18n_sample
$ python manage.py runserver
```

## Routing URLs
- http://localhost:8000/polls

Automatically selected according to the priority of the language used to display the web page. Chinese (zh_Hans,zh_Hant) is also displayed normally.

- http://localhost:8000/(locale_id)/polls

| locale_id        | language       | supported |
| :--------------: | :---------------: | :---------------: |
| ja | Japanese (日本語) | OK |
| ko | Korean (韓国語) | OK |
| zh_Hans | Chinese, Simplified (簡体字) | NG |
| zh_Hant | Chinese, Traditional (繁体字) | NG |

## How to add new language

```
$ django-admin.py makemessages -l (locale_id)
$ vi (path-to-locale-dir)/(locale_id)/LC_MESSAGES/django.po
   :
$ python manage.py compilemessages 
```
