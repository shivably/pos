## Setup for development

Download, prepare virtual python environment and install dependencies 
```shell
git clone https://github.com/shivably/pos.git
cd pos
python -m venv env
source venv/bin/activate  # On Windows use `env\Scripts\activate`
pip install -r requirements
```
    
Create empty database tables (by default a very inefficient SQLite database,
modify `settings.py` to change that):
```
./manage.py migrate
```

Create a super user account.
```
./manage.py createsuperuser
```

Start Django's built-in debugging server:
```
./manage.py runserver
```

Point your web browser to http://127.0.0.1:8000 and enjoy!