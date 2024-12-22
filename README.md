# Expo Camera API Asynchronous Access Bug

This repository demonstrates a bug encountered when using the Expo Camera API and asynchronously accessing camera properties before initialization.  The bug leads to undefined values or unexpected behavior. This README provides details on reproducing the issue and its solution.

## Reproducing the Bug

1. Clone this repository.
2. Run `npm install`.
3. Run `expo start`.
4. Observe the console logs and potential crashes or unexpected behavior associated with attempting to access camera properties before the camera is fully ready.

## Solution

The provided solution uses async/await and promises to ensure that the camera is fully initialized before accessing its properties.  This approach ensures that access attempts only occur after a successful camera initialization, preventing undefined values or crashes.

## Additional Notes

This bug highlights the importance of properly handling asynchronous operations in React Native apps using the Expo Camera API.  Always ensure that your code waits for the camera to fully initialize before attempting to access any of its attributes.