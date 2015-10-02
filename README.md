# web-push
> Web Push library for Node.js

Supports Firefox 43+ and Chromium/Chrome 42+.
Notification with payloads are currently only supported in Firefox (see https://code.google.com/p/chromium/issues/detail?id=486040 for the status in Chromium).

[![Build Status](https://travis-ci.org/marco-c/web-push.svg)](https://travis-ci.org/marco-c/web-push)
[![dependencies](https://david-dm.org/marco-c/web-push.svg)](https://david-dm.org/marco-c/web-push)
[![devdependencies](https://david-dm.org/marco-c/web-push/dev-status.svg)](https://david-dm.org/marco-c/web-push#info=devDependencies)

## sendNotification(endpoint, userPublicKey, payload)

Send a Push notification to an endpoint. *userPublicKey* and *payload* can be undefined, if you want to send a notification without a message.
- *endpoint* is the endpoint URL;
- *userPublicKey* is the public key of the browser;
- *payload* is the message to attach to the notification.

## encrypt(userPublicKey, payload)

Encrypts the payload according to the [Message Encryption for Web Push](https://tools.ietf.org/html/draft-thomson-webpush-encryption-00) standard.
- *userPublicKey* is the public key of the browser;
- *payload* is the message to attach to the notification.

## setGCMAPIKey(apiKey)

Sets the GCM API key that the library should use in making requests to GCM endpoints (in Chromium/Google Chrome).
- *apiKey* is your GCM API key, you can obtain it from the Google Developer Console.

## Projects using web-push

- TicTacToe with offline and Push support using Service Workers - https://github.com/marco-c/tictactoe
