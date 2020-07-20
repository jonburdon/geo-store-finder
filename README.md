* installed django

* created app nearbyshops

* added a line in settings `'django.contrib.gis',`

Error:
```
  File "/workspace/.pip-modules/lib/python3.8/site-packages/django/contrib/gis/gdal/prototypes/ds.py", line 9, in <module>
    from django.contrib.gis.gdal.libgdal import GDAL_VERSION, lgdal
  File "/workspace/.pip-modules/lib/python3.8/site-packages/django/contrib/gis/gdal/libgdal.py", line 39, in <module>
    raise ImproperlyConfigured(
django.core.exceptions.ImproperlyConfigured: Could not find the GDAL library (tried "gdal", "GDAL", "gdal2.4.0", "gdal2.3.0", "gdal2.2.0", "gdal2.1.0", "gdal2.0.0"). Is GDAL installed? If it is, try setting GDAL_LIBRARY_PATH in your settings.
```

* tried `apt-get install gdal-bin`

Error:

```
gitpod /workspace/geo-store-finder $ git commit "Initial Commit"
error: pathspec 'Initial Commit' did not match any file(s) known to git

```

* Updated .gitpod.yml using `gp open .gitpod.yml`

```
image:
  file: .gitpod.dockerfile
tasks:
 - init: . ${GITPOD_REPO_ROOT}/.theia/init_tasks.sh    
vscode:
  extensions:
    - ms-python.python@2019.8.30787:TnGEOx35GXMhyKLjDGz9Aw==
    - formulahendry.auto-close-tag@0.5.6:oZ/8R2VhZEhkHsoeO57hSw==
    - mkaufman.HTMLHint@0.6.0:TdNYbCmjW8N3yiaPW4/adg==
    - eventyret.bootstrap-4-cdn-snippet@1.6.0:AtNd6GnbCYVpmUkOaFXs3A==
    - esbenp.prettier-vscode@4.3.0:jkl8NYpF/GzsahVpjggK0Q==
    - kevinglasson.cornflakes-linter@0.4.0:Sgfmpf9YWoF5/BDJu2xn0w==

FROM gitpod/workspace-full
USER gitpod
RUN sudo apt-get update -q && \
    sudo aptitude install gdal-bin libgdal-dev
    sudo aptitude install python3-gdal
    sudo aptitude install binutils libproj-dev
    docker run --name=postgis -d -e POSTGRES_USER=user999 -e POSTGRES_PASS=123456789 -e POSTGRES_DBNAME=gis -p 5432:5432 kartoza/postgis:9.6-2.4
```




```
  File "/workspace/.pip-modules/lib/python3.8/site-packages/django/contrib/gis/gdal/libgdal.py", line 39, in <module>
    raise ImproperlyConfigured(
django.core.exceptions.ImproperlyConfigured: Could not find the GDAL library (tried "gdal", "GDAL", "gdal2.4.0", "gdal2.3.0", "gdal2.2.0", "gdal2.1.0", "gdal2.0.0"). Is GDAL installed? If it is, try setting GDAL_LIBRARY_PATH in your settings.
```