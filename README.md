## For lost admin name
> python manage.py shell
>> from django.contrib.auth import get_user_model
>> list(get_user_model().objects.filter(is_superuser=True).values_list('username', flat=True))

## For changing username password
> python manage.py changepassword *username*

## How to all the username through shell
> python manage.py shell
>> from django.contrib.auth.models import User
>> all_users = User.objects.all()
>> for user in all_users:
    print(user.username)

