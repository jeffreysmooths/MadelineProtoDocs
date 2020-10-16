---
title: danog\MadelineProto\Ipc\ServerCallback: IPC callback server.
description: 

---
# `danog\MadelineProto\Ipc\ServerCallback`
[Back to index](../../../index.md)

> Author: Daniil Gentili <daniil@daniil.it>  
  

IPC callback server.  




## Constants
* `danog\MadelineProto\Ipc\ServerCallback::SHUTDOWN`: Shutdown server.


## Method list:
* `setIpcPath(\danog\MadelineProto\SessionPaths $session): void`
* `startMe(\danog\MadelineProto\SessionPaths $session): \Amp\Promise`
* `waitShutdown(): \Amp\Promise`
* `loop(): \Generator`
* `setSettings(\danog\MadelineProto\Settings\Ipc $settings): self`
* `isRunning(): bool`
* `signal(mixed|\Throwable $what): void`
* `waitSignal(\Promise|\Generator $promise): \Promise`

## Methods:
### `setIpcPath(\danog\MadelineProto\SessionPaths $session): void`

Set IPC path.


Parameters:
* `$session`: `\danog\MadelineProto\SessionPaths` Session  


#### See also: 
* [`\danog\MadelineProto\SessionPaths`: Session path information.](../SessionPaths.md)




### `startMe(\danog\MadelineProto\SessionPaths $session): \Amp\Promise`

Start IPC server in background.


Parameters:
* `$session`: `\danog\MadelineProto\SessionPaths` Session path  


#### See also: 
* [`\danog\MadelineProto\SessionPaths`: Session path information.](../SessionPaths.md)
* `\Amp\Promise`




### `waitShutdown(): \Amp\Promise`

Wait for shutdown.


#### See also: 
* `\Amp\Promise`




### `loop(): \Generator`

Main loop.


#### See also: 
* `\Generator`




### `setSettings(\danog\MadelineProto\Settings\Ipc $settings): self`

Set IPC settings.


Parameters:
* `$settings`: `\danog\MadelineProto\Settings\Ipc` IPC settings  


#### See also: 
* [`\danog\MadelineProto\Settings\Ipc`: IPC server settings.](../Settings/Ipc.md)




### `isRunning(): bool`

Check whether loop is running.



### `signal(mixed|\Throwable $what): void`

Send signal to loop.


Parameters:
* `$what`: `mixed|\Throwable` Data to signal  


#### See also: 
* `\Throwable`




### `waitSignal(\Promise|\Generator $promise): \Promise`

Resolve the promise or return|throw the signal.


Parameters:
* `$promise`: `\Promise|\Generator` The original promise or generator  
  Full type:
  ```
  \Promise<\T>|\Generator<mixed, \Promise|array<array-key, \Promise>, mixed, \Promise<\T>|\T>
  ```


Fully typed return value:
```
\Promise<\T|mixed>
```
#### See also: 
* `\Promise`
* `\Generator`
* `\T`




---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)