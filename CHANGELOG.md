# Changelog for Palaver ZNC Module

## 1.1.2

### Bug Fixes

- Fix issue where local notifications may appear twice.

## 1.1.1

### Bug Fixes

- Compilation will now respect the `CXX` environment variable so that Palaver
  ZNC will be tested against the configured compiler.

## 1.1.0

### Enhancements

- Push notifications are now sent for CTCP ACTIONs (`/me` messages).
- Support for FreeBSD has been added.
- Push notifications are no longer sent for NOTICEs that are received before
  registering with the IRC server.

  For example, the following NOTICEs will not send push notifications while
  connecting:

  - Looking up your hostname...
  - Checking Ident
  - Found your hostname
  - Got Ident response

- We no longer mention you with private NOTICEs, these are usually server or
  service notices and rarely from a real user.

- You can now disable showing message previews in the Palaver app which will
  prevent the message contents from being sent as a push notification.

### Bug Fixes

- We now detect when building the module with an unsupported compiler and will
  now produce an error. This detects compilers that do not have a correct regex
  implementation.
- Prevents stripping colour codes from messages incoming IRC messages.
- ZNC will no longer send push notifications to backgrounded Palaver devices.


## 1.0.1

### Bug Fixes

- Fixes a timing issue where the push notification may not be sent due to ZNC
  disconnecting from the push notification server before the request was
  processed.


## 1.0.0

Initial version.
