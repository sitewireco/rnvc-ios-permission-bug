Steps:

- install expo example app with: `npx create-expo-app rnvc-ios-perm-repro`
- navigate to prohect: `cd rnvc-ios-perm-repro`
- install rnvc (4.4.2): `npx expo install react-native-vision-camera`
- modify code:
  edit /app/(tabs)/index.tsx with:
  ```
    ...
    import { Camera } from 'react-native-vision-camera';
    import { useEffect } from 'react';
    ...

    export default function HomeScreen() {
      useEffect(() => {
        console.log('foobar')
        if (false) {
          c = Camera
        }
      }, [])

      ...
    }
  ```
- prebuild: `npx expo prebuild`
- run on device (not simulator): `npx expo run:ios --device`

A prompt for permissions appears, even though it is impossible for the codepath to reach the Camera invocation.
