---
title: messages.getChatInviteImporters
description: messages.getChatInviteImporters parameters, return type and example
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_getChatInviteImporters.html
---
# Method: messages.getChatInviteImporters
[Back to methods index](index.md)



### Parameters:

| Name     |    Type       | Required |
|----------|---------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](../types/InputPeer.md) | Optional|
|link|[string](../types/string.md) | Yes|
|offset\_date|[int](../types/int.md) | Yes|
|offset\_user|[Username, chat ID, Update, Message or InputUser](../types/InputUser.md) | Optional|
|limit|[int](../types/int.md) | Yes|


### Return type: [messages.ChatInviteImporters](../types/messages.ChatInviteImporters.md)

### Can bots use this method: **YES**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages_ChatInviteImporters = $MadelineProto->messages->getChatInviteImporters(['peer' => InputPeer, 'link' => 'string', 'offset_date' => int, 'offset_user' => InputUser, 'limit' => int, ]);
```

Or, if you're into Lua:

```lua
messages_ChatInviteImporters = messages.getChatInviteImporters({peer=InputPeer, link='string', offset_date=int, offset_user=InputUser, limit=int, })
```
