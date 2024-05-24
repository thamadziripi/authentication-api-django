# JWT (JSON Web Token)

### Understandig JWT Tokens
JSON Web Token, commonly referred to as JWT, is an open standard (RFC 7519) for 
securely transmitting information between parties as a JSON object. The token is 
digitally signed, ensuring its authenticity and integrity. JWTs are primarily 
used to authenticate users, authorize access to certain resources, and exchange 
information securely.

> Django implementation in settings.py
``` python
REST_FRAMEWORK = {
    "DEFAULT_AUTHENTICATION_CLASSES": (
        "rest_framework_simplejwt.authentication.JWTAuthentication"
    ),
    "DEFAULT_PERMISSION_CLASSES": ("rest_framework.permission.IsAuthenticated"),
}

# Specifying how long before JWT access/refresh token expire
SIMPLE_JWT = {
    "ACCESS_TOKEN_LIFETIME": timedelta(minutes=30),
    "REFRESH_TOKEN_LIFETIME": timedelta(days=1),
}
```