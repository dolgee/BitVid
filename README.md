BitVid
======


Installation
============

Download and set up the repository
```
> virtualenv BitVid_ve
> cd BitVid_ve
> git clone https://github.com/CrateMuncher/BitVid.git
> cd BitVid
> source bin/activate
> pip install -r requirements.txt
```

Setup the Database
```
> python manage.py syncdb
> python manage.py migrate
```

Setup the Search
================

Download elasticsearch (elasticsearch.com) and run it with its default configuration:
```
> wget download.elasticsearch.org/elasticsearch/elasticsearch/elasticsearch-0.90.7.tar.gz
> tar -xvf elasticsearch-0.90.7.tar.gz
> elasticsearch-0.90.7/bin/elasticsearch
```

Index the Data
```
python manage.py rebuild_index 
```


And you're ready to go:
```
> python manage.py runserver
```
