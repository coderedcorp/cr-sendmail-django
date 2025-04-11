# cr-sendmail-django

Django email backend which invokes system `sendmail` binary.


## Usage

In your Django settings, set the email backend:

```python
EMAIL_BACKEND = "cr_sendmail.backends.SendmailBackend"
```

You can also specify a path to the `sendmail` binary:

```python
SENDMAIL_BINARY = "/path/to/sendmail"
```

## Logging

This package uses Python logging to logger named `cr-sendmail-django`. To see log output, configure [Django logging](https://docs.djangoproject.com/en/stable/howto/logging/).


## Compatibility with `django_sendmail_backend`

This package also provides a compatible `django_sendmail_backend` package, as a drop-in replacement for existing sites without modification.

```python
EMAIL_BACKEND = "django_sendmail_backend.backends.EmailBackend"
```

## Credits

This package is a replacement for `django_sendmail_backend`, supported by CodeRed.

Thanks to:
* https://github.com/perenecabuto/django-sendmail-backend
* https://djangosnippets.org/snippets/1864/
