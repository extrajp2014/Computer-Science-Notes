* Install Django in anaconda environment
```bash
# exit current anaconda environment
conda deactivate
# start install
conda create -n cspt5env python=3.8.1 anaconda
conda activate djangoenv
conda install -c anaconda django  
django-admin startproject repository_name
cd repository_name
```

* Run server
```bash
python3 manage.py runserver
```