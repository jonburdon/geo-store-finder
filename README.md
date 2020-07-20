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