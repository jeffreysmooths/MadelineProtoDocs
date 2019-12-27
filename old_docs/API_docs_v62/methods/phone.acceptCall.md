---
title: phone.acceptCall
description: Accept incoming call
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Method: phone.acceptCall  
[Back to methods index](index.md)


Accept incoming call

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[InputPhoneCall](../types/InputPhoneCall.md) | The call to accept | Yes|
|g\_b|[bytes](../types/bytes.md) | [Parameter for E2E encryption key exchange »](https://core.telegram.org/api/end-to-end/voice-calls) | Yes|
|key\_fingerprint|[long](../types/long.md) | You cannot use this method directly, see https://docs.madelineproto.xyz#calls for more info on handling calls | Yes|
|protocol|[PhoneCallProtocol](../types/PhoneCallProtocol.md) | Phone call settings | Yes|


### Return type: [phone\_PhoneCall](../types/phone_PhoneCall.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$phone_PhoneCall = $MadelineProto->phone->acceptCall(['peer' => InputPhoneCall, 'g_b' => 'bytes', 'key_fingerprint' => long, 'protocol' => PhoneCallProtocol, ]);
```

Or, if you're into Lua:

```lua
phone_PhoneCall = phone.acceptCall({peer=InputPhoneCall, g_b='bytes', key_fingerprint=long, protocol=PhoneCallProtocol, })
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|CALL_ALREADY_ACCEPTED|The call was already accepted|
|400|CALL_ALREADY_DECLINED|The call was already declined|
|400|CALL_PEER_INVALID|The provided call peer object is invalid|
|400|CALL_PROTOCOL_FLAGS_INVALID|Call protocol flags invalid|

