---
title: photos.uploadProfilePhoto
description: Updates current user profile photo.
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Method: photos.uploadProfilePhoto  
[Back to methods index](index.md)


Updates current user profile photo.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|file|[File path or InputFile](../types/InputFile.md) | File saved in parts by means of [upload.saveFilePart](../methods/upload.saveFilePart.md) method | Yes|
|caption|[string](../types/string.md) | Caption type | Yes|
|geo\_point|[InputGeoPoint](../types/InputGeoPoint.md) | Location | Optional|
|crop|[InputPhotoCrop](../types/InputPhotoCrop.md) | Cropping info | Yes|


### Return type: [photos\_Photo](../types/photos_Photo.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$photos_Photo = $MadelineProto->photos->uploadProfilePhoto(['file' => InputFile, 'caption' => 'string', 'geo_point' => InputGeoPoint, 'crop' => InputPhotoCrop, ]);
```

Or, if you're into Lua:

```lua
photos_Photo = photos.uploadProfilePhoto({file=InputFile, caption='string', geo_point=InputGeoPoint, crop=InputPhotoCrop, })
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|FILE_PARTS_INVALID|The number of file parts is invalid|
|400|IMAGE_PROCESS_FAILED|Failure while processing image|
|400|PHOTO_CROP_FILE_MISSING|Photo crop file missing|
|400|PHOTO_CROP_SIZE_SMALL|Photo is too small|
|400|PHOTO_EXT_INVALID|The extension of the photo is invalid|

