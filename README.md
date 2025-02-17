# react-native-vpn-detection

## Getting started

`$ npm install react-native-vpn-detection --save`

### Mostly automatic installation

`$ react-native link react-native-vpn-detection`

### Manual installation

#### iOS

1. In XCode, in the project navigator, right click `Libraries` ➜ `Add Files to [your project's name]`
2. Go to `node_modules` ➜ `react-native-vpn-detection` and add `RNNativeVpnDetect.xcodeproj`
3. In XCode, in the project navigator, select your project. Add `libRNNativeVpnDetect.a` to your project's `Build Phases` ➜ `Link Binary With Libraries`
4. Run your project (`Cmd+R`)<

#### Android

1. Open up `android/app/src/main/java/[...]/MainActivity.java`

- Add `import com.reactlibrary.RNNativeVpnDetectPackage;` to the imports at the top of the file
- Add `new RNNativeVpnDetectPackage()` to the list returned by the `getPackages()` method

2. Append the following lines to `android/settings.gradle`:
   ```
   include ':react-native-vpn-detection'
   project(':react-native-vpn-detection').projectDir = new File(rootProject.projectDir, 	'../node_modules/react-native-vpn-detection/android')
   ```
3. Insert the following lines inside the dependencies block in `android/app/build.gradle`:
   ```
     compile project(':react-native-vpn-detection')
   ```

## Usage

```javascript
* Import Library
import Security from "react-native-vpn-detection";

* Example Usage
async function checkSecurity() {
	let detectVPN = await Security.detectVPN().then(response => { return response });
	let detectProxy = await Security.detectProxy().then(response => { return response });
}
checkSecurity();
```
