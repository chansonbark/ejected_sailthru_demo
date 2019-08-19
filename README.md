This is a test application to demo installation of the Sailthru Push SDK in an ios React Native app that has been ejected to a "bare" app from Expo.
This application utilizes certain unimodules that work in the bare workflow, but not after editing the ios AppDelegate.m file.

To test:
1) checkout the repository and run `yarn install`
2) cd ios/ and run `pod install`
3) back out to the root directory and run `yarn run ios`

The application should start and ask for push notification permission. It should then crash with the following error:
```
Possible Unhandled Promise Rejection (id: 0):
Error: The method or property Amplitude.initialize is not available on ios, are you sure you've linked all the native dependencies properly?
```

It similarly fails for other packages if the source of the error is removed one at a time.
