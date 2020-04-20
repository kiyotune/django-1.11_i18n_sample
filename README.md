 $ git clone https://github.com/kiyotune/django-1.11_i18n_sample
 $ cd django-1.11_i18n_sample
 $ python manage.py runserver


 http://localhost:8000/polls
 http://localhost:8000/ja/polls
 http://localhost:8000/en/polls
 http://localhost:8000/(locale_id)/polls

The display language is automatically selected according to the priority of the language used to display the web page.
 
* How to add language-setting

 $ django-admin.py makemessages -l ja
 $ vi (path-to-locale-dir)/ja/LC_MESSAGES/django.po
    :(edit)
 $ python manage.py compilemessages

