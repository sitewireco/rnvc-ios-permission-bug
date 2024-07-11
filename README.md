# Reproduction (minimal) of RNVC issue in iOS
This repository exists solely to represent and issue in 4.2.x (and possibly previous) versions of RNVC, where an iOS device will prompt for camera permissions if any code references the imported `Camera` object from rnvc, even if that code path is not hit.

## Reproduction steps
Listed in /repro_steps.md

## logs
In repro /rnvc-repro-logs

These logs were captured from console starting just before the expo run code wsa executed and compiled, until the app had loaded and logged "foobar" into console.

## code changes
This is a stock expo example app, with just the homescreen modified to import RNVC, and utilize a useEffect to reference the Camera object in a code-path that will never be executed.
