# users/signup Endpoint

The users/signup endpoint creates a user account on plug.dj.

### Endpoint

**users/signup**

### Method

_POST_

### Parameters

**csrf**: Cross Site Request Forgery token

**username**: Your username

**email**: Your email

**password**: Your password

**response**: reCAPTCHA response

```json
{
	"csrf": "xxxxx",
	"username": "xxx",
	"email": "xxx@xxx.com",
	"password": "xxxxxxxx",
	"response": "xxxxx"
}
```

### Possible error messages

CSRF token has expired
```json
{
	"data": [
		"This CSRF token has expired."
	],
	"meta": {},
	"status": "csrfTokenExpired",
	"time": "xx.xxxxxxxxxxx"
}
```

CSRF token is invalid
```json
{
	"data": [
		"This CSRF token is invalid."
	],
	"meta": {},
	"status": "csrfTokenInvalid",
	"time": "xx.xxxxxxxxxxx"
}
```

reCAPTCHA response is invalid
```json
{
	"data": [
		"This request was understood but is forbidden."
	],
	"meta": {},
	"status": "recaptchaError",
	"time": "xx.xxxxxxxxxxx"
}
```

Password is too short (8 chars. minimum)
```json
{
	"data": [
		{
			"password": [
				"passwordShort"
			]
		}
	],
	"meta": {},
	"status": "requestError",
	"time": "xx.xxxxxxxxxxx"
}
```

Email is taken
```json
{
	"data": [
		{
			"email": [
				"emailTaken"
			]
		}
	],
	"meta": {},
	"status": "requestError",
	"time": "xx.xxxxxxxxxxx"
}
```

Username is taken
```json
{
	"data": [
		"Email or username already taken"
	],
	"meta": {},
	"status": "requestError",
	"time": "xx.xxxxxxxxxxx"
}
```

### Data returned

```js
{
  'data': [],
  'meta': {},
  'status': 'ok',
  'time': 'xx.xxxxxxxxxxx'
}
```
