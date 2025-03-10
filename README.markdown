__OpenCV computer vision with iOS: stitching panoramas__  

<img src = "https://github.com/foundry/OpenCVSwiftStitch/blob/meta/meta/example.big.jpg">

Version 5.0 of [OpenCVStitch](http://github.com/foundry/OpenCVStitch) - updated for Swift 5.0  + OpenCV 4.7  
See appropriate branches and tags for Swift 2.x - 4.x

This project was created to a answer a couple of Stack Overflow questions:  
[libraries to CAPTURE panorama in iOS](http://stackoverflow.com/q/14062932/1375695)  
[Can I mix Swift with C++? Like the Objective - C .mm files](http://stackoverflow.com/q/24042774/1375695)    

v2 demonstrates how to mix Swift, Objective-C and C++ in one project whilst keeping the code clearly separate. 

The project AppDelegate and View Controller are written in Swift. Swift cannot talk directly to C++ (which we need for OpenCV), so we provide an Objective-C++ wrapper class to mediate between Swift and C++. We also provide an Objective-C++ category on UIImage to mediate between UIImage and CV::Mat image formats. The CVWrapper header file is pure Objective-C. For [v1](https://github.com/foundry/OpenCVStitch)(which doesn't use Swift) this separation was a matter of clean style. For v2, it is a requirement: if any C++ headers are included in the wrapper, the app will not compile (Swift won't like it).

__Installation__  
To run the project you need to install the OpenCV framework using Cocoapods    

Assuming you have first [installed CocoaPods](https://guides.cocoapods.org/using/getting-started.html), run 'pod install' in this directory to install OpenCV for the project. From then on, always open the project in XCode from the `SwiftStitch.xcworkspace` file that the pod install creates. 

The podfile will install openCV v4.7.0. 


__Use__  
OpenCVStitch is a very simple iOS/openCV example showing basic use of the Stitcher class. The c++ code is adapted from a sample included with the openCV distribution.  

The app has almost no user interface. On launch, the stitching code operates on four sample images, displaying the result in a UIScrollView.

__OpenCVSwiftStitch Versions__   
[Version 5.1](https://github.com/foundry/OpenCVSwiftStitch/releases/tag/5.1)  
Swift / Objective-C / C++   
OpenCV 4.7  
Modern Swift - async / await  
Error, exception handling from C++ -> Objective-C -> Swift  
Tested with XCode 13.2 / Swift 5.0 for iOS 13.0+  
[Version 5.0](https://github.com/foundry/OpenCVSwiftStitch/releases/tag/5.0)  
Swift / Objective-C / C++   
OpenCV 4.3  
Tested with XCode 12.0 / Swift 5.0 for iOS 9.0+  
[Version 4.0](https://github.com/foundry/OpenCVSwiftStitch/releases/tag/4.0)   
Swift / Objective-C / C++   
Tested with XCode 10.0 / Swift 4.2 for iOS 8.0+  
[Version 3.0](https://github.com/foundry/OpenCVSwiftStitch/releases/tag/3.0)   
Swift / Objective-C / C++   
Tested with XCode 8.0 / Swift 3.0 for iOS 8.0+  
[Version 2.1](https://github.com/foundry/OpenCVSwiftStitch)   
Swift / Objective-C / C++   
Tested with XCode 7.0 / Swift 2.0 for iOS 7.0+  
[Version 2.0](https://github.com/foundry/OpenCVSwiftStitch/tree/v2.0)   
Swift / Objective-C / C++   
Tested with XCode 6.4 / Swift 1.2 for iOS 7.0+  
[Version 1.0](https://github.com/foundry/OpenCVStitch)  
Objective-C / C++   
Tested with XCode 4.5.2 -> 6.3 for iOS 5.1 upwards   

Provides a partial answer to: [Libraries to capture panoramas in iOS 6](http://stackoverflow.com/questions/14062932/libraries-to-capture-panorama-in-ios-6/14064788#14064788) (Stack Overflow)

__OpenCV Versions__

_OpenCV 4.7_

The original repo used OpenCV 4.3 however there is newer version 4.7 which is used in this fork
The podfile installs OpenCV 4.7

__XCode 12__  

Project is now updated for Swift 5.0 and XCode 12. For backwards compatibility checkout the 2.0 / 2.1 branches, 3.0 /4.0 releases or refer to the Objective-C version v1.0.

__Comparisons__

Here is the comparision between OpenCV 3.0 and 4.3 but as stated above this fork usede 4.7. I won't do the comparision between 4.3 and 4.7 because I am lazy (but there was a positive difference in newer version I swear...)
<table><tr>
<td>OpenCV 2.4.9</td><td>OpenCV 3.0.0</td><td>OpenCV 3.1.0</td><td>OpenCV 4.3.0</td>
</tr><tr>
<td>
<img src="https://github.com/foundry/OpenCVSwiftStitch/blob/meta/meta/v2_inset2.jpg"  width="200" height="240" alt="v2_inset2">


</td>
<td>
<img src="https://github.com/foundry/OpenCVSwiftStitch/blob/meta/meta/v3_inset2.jpg" width="200" height="240" alt="v3_inset2">


</td>
<td>
<img src="https://github.com/foundry/OpenCVSwiftStitch/blob/meta/meta/v3.1_inset2.jpg" width="200" height="240" alt="v3.1_inset2">


</td>
<td>
<img src="https://github.com/foundry/OpenCVSwiftStitch/blob/meta/meta/v5_inset2.jpg" width="200" height="240" alt="v5_inset2">


</td>
</tr><tr>
<td>
<img src="https://github.com/foundry/OpenCVSwiftStitch/blob/meta/meta/v2_inset.jpg" width="200" height="240" alt="v2_inset2">

</td>
<td>
<img src="https://github.com/foundry/OpenCVSwiftStitch/blob/meta/meta/v3_inset.jpg" width="200" height="240" alt="v2_inset2">

</td>
<td>
<img src="https://github.com/foundry/OpenCVSwiftStitch/blob/meta/meta/v3.1_inset.jpg" width="200" height="240" alt="v2_inset2">

</td>
<td>
<img src="https://github.com/foundry/OpenCVSwiftStitch/blob/meta/meta/v5_inset.jpg" width="200" height="240" alt="v5_inset2">

</td>
</tr></table>
