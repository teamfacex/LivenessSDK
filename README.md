
[![Build Status](https://img.shields.io/cocoapods/p/LivenessSDK)](https://img.shields.io/cocoapods/p/LivenessSDK)
[![CocoaPods Compatible](https://img.shields.io/cocoapods/v/LivenessSDK)](https://img.shields.io/cocoapods/v/LivenessSDK)
[![Updated](https://img.shields.io/github/last-commit/friendlynandy/LivenessSDK)](https://img.shields.io/github/last-commit/friendlynandy/LivenessSDK)
[![Licence](https://img.shields.io/cocoapods/l/LivenessSDK?color=red&logo=red)](https://img.shields.io/cocoapods/l/LivenessSDK?color=red&logo=red)


# LivenessSDK

## 📜 Introduction
Brought to you by FaceX.io, this iOS LivenessSDK can now be used to integrate gesture-based liveness Detection into your iOS applications.

## 🔧 Functioning
This LivenessSDK is Liveness based on Motion detection. Users will be directed by the screen to perform facial gestures and actions which will be analyzed to verify and identify live visitors. 

## 📑 Index
* [Documentation](#-documentation)
* [Features](#-features)
* [Installation](#-installation)
  * [Cocoapods](#using-cocoapods)
* [How to use](#-how-to-use)
* [Delegates](#-Delegates)
   * [LivenessDelegate](#-LivenessDelegate)
* [Customization](#-customization)
  * [Steps](#-Steps)
  * [Thersholds](#-Thresholds)  
* [Supported OS & SDK Versions](#-supported-os--sdk-versions)
* [License](#-license)

### 📚 Documentation 

- Step 1: Sign up for a developer account through [FaceX User Portal](https://search.facex.io/#/register)
- Step 2: Navigate to Plans & Payments Tab & Select  [Plans](https://search.facex.io/#/home/payments/plans)
- Step 3: Scroll to Mobile SDK, select Active Liveness and provide the necessary details
- Step 4; Purchase a plan matching your license requirement
- Step 4: Navigate to Mobile SDK Tab & Select [License History](https://search.facex.io/#/home/mobilesdk/license)
- Step 5: Download the plist file for iOS SDK from the offline license section
- Step 6: Download the offline Active Livenesss iOS SDK from this Github [LivenessSDKOnline](https://nuclearace.github.io/LivenessSDK/Classes/LivenessSDK.html)
- Step 7: Add the plist file from the portal to your project. 


## 🌟 Features
- Supports iOS 12.0+
- Supports binary
- Supports iPhone and iPad


## 📲 Installation
Requires Swift 4/5 and Xcode 10.x

#### Using [CocoaPods](https://cocoapods.org)

[CocoaPods](https://cocoapods.org) is a dependency manager for Cocoa projects. For usage and installation instructions, visit their website. To integrate Alamofire into your Xcode project using CocoaPods, specify it in your `Podfile`:


Create `Podfile` and add `pod 'LivenessSDK'`:

```ruby
use_frameworks!

target 'YourApp' do
    pod 'LivenessSDK', '~> 0.0.3'
end
```

Install pods:

```
$ pod install
```

Import the module:

Swift:
```swift
import LivenessSDK
```

## 🐒 How to use
```swift
import LivenessSDK

  var liveness = Liveness()

  liveness.delegate = self
 
  liveness.startLiveness()

```
## 🏄 Delegates

#### LivenessDelegate

```swift

 func livenessSuccess(live: Bool) {
  }
  
 func livenessError(live: Bool, error: NSError) {
  }

```

## 🎛 Customization

You can set some properties for liveness.

#### Steps
| Steps | Value | Default | 
| ------- | ------- |------- | 
| **Eyes**(enableEyes)  | `Bool` | `false` | 
| **Mouth**(enableMouth)   | `Bool` | `false` | 
| **Yaw**(enableYaw)   | `Bool` | `false` | 
| **Random Steps**(randomSteps)   | `Bool` | `true` | 


#### Thresholds
| Property | Values | Default | 
| ------- | ------- |------- | 
| **Eyes closed Threshold**(eyeThreshold)  | `0.05...0.2` | `0.1` | 
| **Mouth opened Threshold**(mouthThreshold)   | `0.1...0.6` | `0.35` | 
| **Each step timer**(timerSeconds)   | `Seconds` | `5 seconds` | 




### 📋 Supported OS & SDK Versions
* iOS 12.0+
* iPadOS 13.0+
* Swift 5


## 👮🏻 License
-[Eula]
