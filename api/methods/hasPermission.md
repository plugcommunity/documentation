# Permission/Role Check

Checks whether the specified user has the specified role.

### Example

```js
API.hasPermission(
    ID,
    ROLE
);
```

Real Example:

```js
API.hasPermission(
    3626824,
    API.ROLE.BOUNCER
);
```

Returns `true` if user matches the role, else returns `false`.

### Endpoint

Frontend check only, based on stored user information