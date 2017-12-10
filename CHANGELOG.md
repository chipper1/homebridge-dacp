# Changelog

 ## Version 0.7.0 - 2017-12-17  (planned)

- More reliable reachable status

The reachable status was previously reported when the accessory has seen
MDNS announcements for the Apple TV or iTunes. This version updates the
reachable state depending upon the actual network connection state.

- Made zero the default media type value in the NowPlayingService

This aligns the value with reports from Apple TV, when playing media from apps.
The reported media type is zero in those cases.

- Report actual playback position via getproperty calls instead of guessing

Previous version tried to guess the playback position by essentially counting
the seconds. This version periodically acquires the actual playback position and
updates the characteristic in response to reports from iTunes or Apple TV.

- Now Playing Service shows all characteristics immediately

If nothing was playing most of the characteristics were missing from the now
playing service as they were optional.

## Version 0.0.6 - 2017-12-10

- Implemented exponential backoff to recover broken DACP connections
- Added media type to the NowPlayingService
- Added genre to the NowPlayingService
- Emptying values in the NowPlayingService if Apple TV or iTunes disappears
- Added this change log
- Reworded pairing messages in the log
- Added decoder for 'mers' and 'merr' DMAP messages
- Setting accessory as unreachable if Apple TV or iTunes disappears

## Version 0.0.5 - 2017-12-09

- Write errors to the log when a DACP connection fails

## Version 0.0.4 - 2017-12-08

- Changed license to MIT in package
- Started basic error handling and recovery for DACP connections
- Improved parsing of DMAP message containers
- Basic error handling in DacpClient
- Improved messages in homebridge logs for pairing purposes

## Version 0.0.3 - 2017-12-08

- No changes

## Version 0.0.2 - 2017-12-08

- Added Play/Pause switch to control playback

## Version 0.0.1 - 2017-12-08

- Created initial basic accessory and initial work on DMAP support.