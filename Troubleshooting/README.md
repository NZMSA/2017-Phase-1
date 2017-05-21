# Troubleshooting

<p>

</p>

## Android

### App builds but crashes when deployed

<p>

From time to time you may encounter an issue of your app building without any errors,deploys fine and installs on your device, the app launches but immediately crashes without any real errors in the debug window indicating what the error was. Below are steps you can take to fix such issues.  

</p>

1. Navigate to Settings -> Apps and scroll down until you see 'Xamarin.Android API-[Version Number] Support'. Tap on each and tap 'Uninstall'.

<img src="media/uninstall.png"  width="1024"/>

2. Scroll up until you find 'Mono Shared Runtime' and tap uninstall.

<img src="media/uninstall2.png"  width="1024"/>

3. Look for the name of your Xamarin app and also uninstall it.
4. Inside Visual Studio/Xamarin Studio, right click on your Android project, click 'Rebuild' and then run the project again.

<p>

If the above steps still don't work for you, try disabling 'Shared Mono Runtime' from Visual Studio/Xamarin Studio.

NOTE: The screenshots below are from Visual Studio 2017 for Mac however, the steps are more or less identical on Windows.

</p>

5. Right click on your Android project and click 'Options'.

<img src="media/sharedmono1.png"  width="1024"/>

6. Under 'Android Build', make sure 'Use Shared Mono Runtime' is unchecked. Click 'OK' when you're done. 

<img src="media/sharedmono2.png"  width="1024"/>

7. Now repeat steps 1-4 and you should be good.

### TargetFrameworkVersion package issue

<p>

```
The $(TargetFrameworkVersion) for Xamarin.Forms.Platform.Android.dll (v7.1) is greater than the $(TargetFrameworkVersion) for your project (v6.0). You need to increase the $(TargetFrameworkVersion) for your project.
```

If you see a message like this while trying to build and deploy your Android project, you may need to update your NuGet packages. The above message indicates you should update your Xamarin.Forms NuGet package in your Android project. The steps to do that are as follows.

</p>

1. Expand your android project and you should see a folder called 'Packages'. Expand that and you should see all the NuGet packages for that project.

2. Look for 'Xamarin.Forms'. Right click and click on 'Update'.

<img src="media/upgradeforms.png"  width="1024"/>

3. OPTIONAL - While you're at it, you might as well update all NuGet packages across all projects. To do that, right click on your solution, and click 'Update NuGet Packages'. This may take some time depending on your internet connection.

 <img src="media/upgradepackages.png"  width="1024"/>

 ### Emulator issues

 <p>

On Windows, if you're having issues running the emulator you may need to enable Hyper-V (if your device supports it). Each machine is different so in order to enable Hyper-V you will need to do a quick Bing search on how to do that for your specific make and model. 

Alternatively, the easiest and (in my opinion) the best way to deploy and debug your app is using an actual Android device. But before you can do that, you'll need to enable a couple things on that device first before you can use it for debugging.

NOTE: I will be using a Nexus 6P running Android O DP 2. However, the steps will be more or less the same regardless.

 </p>

 1. On your Android device, navigate to 'Settings' -> 'System' -> 'About phone' and scroll down until you see 'Build number'. Tap on it about 7 times and you'll get a popup letting you know developer mode has been enable.

 <img src="media/developermode.png"  width="1024"/>

 2. Navigate back one and you should now see 'Developer options'. Tap on it, make sure developer mode is turned on, scroll down until you see 'USB debugging' and make sure it's switched on.

 <img src="media/developermode2.png"  width="1024"/>

 3. Now inside Visual Studio/Xamarin Studio you should be able to see your physical device as option to deploy your app to. 