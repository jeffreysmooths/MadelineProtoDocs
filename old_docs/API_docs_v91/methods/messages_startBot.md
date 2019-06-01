---
title: messages.startBot
description: Start a bot
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Method: messages.startBot  
[Back to methods index](index.md)


Start a bot

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|bot|[Username, chat ID, Update, Message or InputUser](../types/InputUser.md) | The bot's ID or username | Optional|
|peer|[Username, chat ID, Update, Message or InputPeer](../types/InputPeer.md) | Where to start the bot (@me or group ID/username) | Optional|
|start\_param|[string](../types/string.md) | The bot's start parameter | Yes|


### Return type: [Updates](../types/Updates.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
define('MADELINE_BRANCH', '');
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Updates = $MadelineProto->messages->startBot(['bot' => InputUser, 'peer' => InputPeer, 'start_param' => 'string', ]);
```

Or, if you're into Lua:

```lua
Updates = messages.startBot({bot=InputUser, peer=InputPeer, start_param='string', })
```

### Errors this method can return:

| Error    | Description   |
|----------|---------------|
|BOT_INVALID|This is not a valid bot|
|PEER_ID_INVALID|The provided peer id is invalid|
|START_PARAM_EMPTY|The start parameter is empty|
|START_PARAM_INVALID|Start parameter invalid|

