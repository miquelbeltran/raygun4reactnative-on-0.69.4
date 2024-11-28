## Installing raygun4reactnative on React-Native version `0.69.4`

First: Create a project with `0.69.4`: 

```
npx react-native init MyProject --version 0.69.4
```

Attempting to run the project now will show the following error:

```
 BUNDLE  ./index.js 

 ERROR  Error: [@RNC/AsyncStorage]: NativeModule: AsyncStorage is null.

To fix this issue try these steps:

  • Uninstall, rebuild and restart the app.

  • Run the packager with `--reset-cache` flag.

  • If you are using CocoaPods on iOS, run `pod install` in the `ios` directory, then rebuild and re-run the app.

  • Make sure your project's `package.json` depends on `@react-native-async-storage/async-storage`, even if you only depend on it indirectly through other dependencies. CLI only autolinks native modules found in your `package.json`.
```

This needs to be fixed by installing `@react-native-async-storage/async-storage` directly in the project.

Also, you need to install an old version, I recommend the same version that `raygun4reactnative` uses:

```
npm install @react-native-async-storage/async-storage@^1.13.4
```

Then, you can procede with building the project:

```
npx react-native run-android
```

And then

```
npx react-native start
```

Then press `d` to launch the project
