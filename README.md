![Concentric Sky](https://concentricsky.com/media/uploads/images/csky_logo.jpg)


# Sky Redirects

Sky Redirects is an open-source Django library developed by [Concentric Sky](http://concentricsky.com/). It allows creation and editing of URL redirect patterns in Django's admin interface.


## Installation and Usage

Install the library using pip:

    pip install git+https://github.com/concentricsky/django-sky-redirects.git


Add 'sky_redirects' to INSTALLED_APPS in settings.py:

```python
   INSTALLED_APPS = (
      'sky_redirects',
      ...
```

Add the sky_redirects middleware to the *beginning* of MIDDLEWARE_CLASSES in settings.py::

```python
    MIDDLEWARE_CLASSES = [
      'sky_redirects.middleware.DomainRedirectMiddleware',
      'sky_redirects.middleware.RegexRedirectMiddleware',
      ...
   ]
```

Once you run syncdb, you will be ready to add redirects in the admin interface and you are done.


## License

This project is licensed under the Apache License, Version 2.0. Details can be found in the LICENSE.md file.


## About Concentric Sky

_For nearly a decade, Concentric Sky has been building technology solutions that impact people everywhere. We work in the mobile, enterprise and web application spaces. Our team, based in Eugene Oregon, loves to solve complex problems. Concentric Sky believes in contributing back to our community and one of the ways we do that is by open sourcing our code on GitHub. Contact Concentric Sky at hello@concentricsky.com._
