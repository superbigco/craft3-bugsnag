# Changelog

## 5.0.0-beta.1 - 2024-03-04

### Changed
- Now requires PHP `8.2.0+`.
- Now requires Craft `5.0.0-beta.1+`.

## 4.0.1 - 2023-10-25

### Added
- Add plugin settings warnings when set via the config file.

### Changed
- Only admins are now allowed to access plugin settings.

### Fixed
- Fix being unable to modify blacklist items in the control panel settings.

## 4.0.0 - 2022-07-19

### Changed
- Now requires PHP `8.0.2+`.
- Now requires Craft `4.0.0+`.

## 3.0.2 - 2022-07-19

### Added
- Allow appropriate plugin settings to be set via `.env` variables.

### Fixed
- Fix settings page in control panel not working.

## 3.0.1 - 2022-07-19

### Added
- Add `craft.bugsnag.handleException()`.

## 3.0.0 - 2022-07-18

> {note} The plugin’s package name has changed to `verbb/bugsnag`. Bugsnag will need be updated to 3.0 from a terminal, by running `composer require verbb/bugsnag && composer remove superbig/craft3-bugsnag`.

### Changed
- Migration to `verbb/bugsnag`.
- Now requires Craft 3.7+.

## 2.1.2 - 2020-05-31

### Fixed
- Fixed namespace that causes PSR warning

## 2.1.1 - 2020-04-16

### Added
- Added `craft.bugsnag.getBrowserConfig()` to get the config needed for the Bugsnag JS client

### Fixed
- Fixed passing empty `releaseStage` value

## 2.1.0 - 2020-04-16

### Added
- Added ability to set metadata on the fly by calling `{% do craft.bugsnag.metadata({ order: 1234 }) %}`. Note that this has to be done before the frontend asset is included

### Changed
- Upgraded the Bugsnag client to v7

### Fixed
- Fixed user reporting

## 2.0.6 - 2020-01-22

### Added
- Added `getClient` method to service. This exposes the client to other plugins / modules.
- Added `browserApiKey` for configuring frontend reporting

### Changed
- Parse `browserApiKey` and `serverApiKey` for env variables and aliases

### Fixed
- Fixed frontend Bugsnag asset to comply with the latest version of JS client

## 2.0.5 - 2019-08-27

### Added
- Added asset bundle to capture JS errors in a more seamless fashion

### Changed
- The plugin can now capture early initialization errors (if manually setup in `app.php`)

### Fixed
- Fixed error when no items were added to exceptions blacklist

## 2.0.4 - 2019-03-14

### Fixed
- Fixed filters support

## 2.0.3 - 2019-03-09

### Added
- Added exceptions blacklist (lets you ignore those 404 errors that clogs up your log)

## 2.0.2 - 2019-02-22

### Added
- Added support for `appVersion`

## 2.0.1 - 2018-07-20

### Fixed
- Fixed check that passes user information to Bugsnag if set
- Fixed error when installing plugin through the console command
- Fixed api config key in config example

## 2.0.0 - 2017-12-08

### Added
- Initial release
