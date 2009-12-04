---
type: rule
title: Do you distribute a product in Release mode?
uri: do-you-distribute-a-product-in-release-mode
created: 2009-05-05T06:48:04.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee

---

 This field should not be null (Remove me when you edit this field). 

```
#if DEBUG MessageBox.Show("Application started"); #endif
```

**Figure: Code that should only run in Debug mode, we certainly don't want this in the release version.**![Debug configuration](/Standards/SoftwareDevelopment/RulesToBetterDotNETProjects/PublishingImages/DebugConfiguration.gif) **Figure: Set "Generate Debugging Information" to True on the project properties page (VS 2003).**![Advanced Build Settings](/Standards/SoftwareDevelopment/RulesToBetterDotNETProjects/PublishingImages/VS2005AdvancedBuildSettings.gif) **Figure: Set "Debug Info" to "pdb-only" on the Advanced Build Settings page (VS 2005).**

| We have a program called [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/Default.aspx#Release) to check for this rule. |
| --- |


