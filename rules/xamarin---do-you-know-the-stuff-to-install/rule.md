---
type: rule
title: Xamarin - Do you know the stuff to install?
uri: xamarin---do-you-know-the-stuff-to-install
created: 2016-08-19T17:53:30.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 ​Installing Visual Studio is not enough.... There is another 2 hours plus of downloading and installing to get to your first successful Xamarin hello world app.
 
### Step 1

Install VS 2015 + the Xamarin extension:  https://msdn.microsoft.com/en-us/library/mt613162.aspx
 ![xamarin-1.png](xamarin-1.png) Figure: You need "C#/.NET (Xamarin v4.1.0)
**Note:** Xamarin Studio doesn't exist on the PC anymore.

### Step 2 - Android SDK Manager (about 2 hours)

This one is painful...
 ![xamarin-2.png](xamarin-2.png) 
Then get all the ones that say "Installed" :
 ![xamarin-3.png](xamarin-3.png) 
### Step 3 - "Manage NuGet Packages for Solution" (about 30 minutes)  


Create a Blank App (xamarin.Forms Portable) project (this way it will trigger grabbing all extra stuff).
Check and ensure Nuget Packages are up to date .
 ![xamarin-4.png](xamarin-4.png)  ![xamarin-5.png](xamarin-5.png) 
### Step 4 - run the app


Actually run the application you’ve created. Ensure it builds. It won't =D well first time it often won't, if it does then congratulations you have got everything!

