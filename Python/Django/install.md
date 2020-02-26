* Install Django in anaconda environment
```bash
# exit current environment
conda deactivate
conda create -n djangoenv python=3.6 anaconda
conda activate djangoenv
conda install -c anaconda django  
django-admin startproject repository_name
cd repository_name
```

* Run server
```bash
python3 manage.py runserver
```
