---
title: auth.sentCodeTypeSms
description: The code was sent via SMS
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: auth.sentCodeTypeSms  
[Back to constructors index](index.md)



The code was sent via SMS

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|length|[int](../types/int.md) | Yes|Length of the code in bytes|



### Type: [auth\_SentCodeType](../types/auth_SentCodeType.md)


### Example:

```php
$auth_sentCodeTypeSms = ['_' => 'auth.sentCodeTypeSms', 'length' => int];
```  


Or, if you're into Lua:

```lua
auth_sentCodeTypeSms={_='auth.sentCodeTypeSms', length=int}

```

