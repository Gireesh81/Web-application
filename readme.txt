My project

structure

myproject/
├── env/            # Python virtual environment (should NOT be committed)
├── frontend/       # React frontend
├── store/          # Django backend
├── ansible/        # We'll create this for deployment scripts
├── Jenkinsfile     # We'll create this for CI steps
└── README.md


set up for Django using linux

1.apt apt update
2.apt install python3.12-venv (installing virtual environment)
   1.mkdir myproject
   2.cd myproject
3.python3 -m venv env (create virtual environment)
4.source env/bin/activate (activate it virtual environment)
5.pip install django (install of django in virtual environment)
6.django-admin startproject store (create a project name store)
7.python manage.py startapp product (create app name product)


APPEND_SLASH = False (for to avoid back slase / in url end)

{
    "username": "giri",
    "email": "giri@gmail.com",
    "password": "giri@81"
}


if token refresh failed check using this
PS E:\myproject\store> python manage.py shell    
>>> from django.contrib.auth.models import User 
>>> User.objects.all()
<QuerySet [<User: Gireesh>, <User: testuser>, <User: giri>]>
>>> user = User.objects.get(username='giri')
>>> print(user.username)
giri
>>> print(user.is_active) 
True
>>> print(user.check_password(giri@81'))
False
>>> user.set_password('giri@81')
>>> user.save()
>>> exit()

{
    "refresh": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0b2tlbl90eXBlIjoicmVmcmVzaCIsImV4cCI6MTc0NDYzNDE1NywiaWF0IjoxNzQ0NTQ3NzU3LCJqdGkiOiI4Y2M4ZTQzYWMwZjk0MzMwYmM4Yzc2ZTY1M2ZmMDBkYyIsInVzZXJfaWQiOjF9.jSsO_bJJKi3rSKfr6LKHVay_83BJT9CrJtgVz2_xiMs",
    "access": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0b2tlbl90eXBlIjoiYWNjZXNzIiwiZXhwIjoxNzQ0NTQ4MDU3LCJpYXQiOjE3NDQ1NDc3NTcsImp0aSI6ImViYTg5Y2EwM2I4YTRlNTk4MzNmMWE5ZDcxZGFjMTFkIiwidXNlcl9pZCI6MX0.KGbMEW2izWy3XpZsp9zlhVryDde_eErboBLOPuazYK0"
}


razorpay

rzp_test_yuvMvuY7LHZm5I   - test key id
kqZ2mq4KnqKbd901K9TMHwBJ  - test key secret


react 

  ➜  press h + enter to show help
h

  Shortcuts
  press r + enter to restart the server
  press u + enter to show server url
  press o + enter to open in browser
  press c + enter to clear console
  press q + enter to quit