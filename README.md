# pygooglehomenotifier

google-home-notifier for python

## Description

This library is that adds voice speech function to PyChromecast. For Python 3.6+.

## Install

```bash
$ pip install pygooglehomenotifier
```

## Usage
    
> **Note**  You need to keep the port open for mdns (5353/udp).

```python
>> import pygooglehomenotifier

>> # Get all googlehomes on your network (use mdns)
>> googlehomes = pygooglehomenotifier.get_googlehomes()
>> # Get googlehome by IP Address
>> googlehomes = pygooglehomenotifier.get_googlehomes(ipaddr = "xxx.xxx.xxx.xxx")
>> # Get googlehomes by friendly name (use mdns)
>> googlehomes = pygooglehomenotifier.get_googlehomes(friendly_name = "xxxxxxx")
>> # Get googlehomes by UUID (use mdns)
>> googlehomes = pygooglehomenotifer.get_googlehomes(uuid = "xxxx-xxxx-xxxx-xxxx")

>> # Wait connecting
>> googlehomes[0].wait()

>> # Notify (asynchronous)
>> googlehomes[0].notify("Test.", lang = "en")
>> # Play mp3 file (asynchronous)
>> googlehomes[0].play("https://xx/xx/xx/xx.mp3")

>> # Suspend playback
>> googlehomes[0].pause()
>> # Resume playback
>> googlehomes[0].resume()
>> # Check if notifing message or playing mp3 file
>> googlehomes[0].is_playing()
>> # Wait for playback to complete
>> googlehomes[0].block_while_playing()
```

## Requirement

- PyChromecast

## Author

[k-sh](https://github.com/k-sh)

## Licence

[MIT](https://github.com/k-sh/pygooglehomenotifier/blob/main/LICENSE)

