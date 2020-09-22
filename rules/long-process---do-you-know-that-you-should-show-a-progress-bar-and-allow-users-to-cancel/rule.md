---
type: rule
title: Long Process - Do you know that you should show a progress bar and allow users to cancel?
uri: long-process---do-you-know-that-you-should-show-a-progress-bar-and-allow-users-to-cancel
created: 2012-11-27T03:05:05.0000000Z
authors: []

---

 
The **last** thing a user wants is to be stuck waiting around for a long-running process to finish that they accidentally started in the first place. This heightens frustration with the application because:

- They do not know how long the process will last (adds uncertainty to the user experience)
- They cannot stop the process (creates lack of control in the user experience)

   ​
Instead, keep users happy with your application by:

- Showing status description information above the progress bar
- Allowing the user to stop the process at any time by clicking "Cancel" (or as a minimum, prompt for confirmation before the long running process starts)

![Progress form with Description & Cancel Button](../../assets/AllowCancelAndShowProgressForLongRunningProcesses.gif)Figure: Good Example - Progress Bar with description and Cancel Button![Progress form with description and status& Cancel Button](../../assets/AllowCancelAndShowProgressForLongRunningProcesses2.jpg)Figure: Good Example - Progress Bar with description and status, and Cancel Button
We have a product called [SSW .NET Toolkit](http://www.ssw.com.au/ssw/NETToolKit/) which includes these controls. [SSW .NET Toolkit - Using Progress bars/Status forms.](http://www.ssw.com.au/ssw/NETToolKit/08ProgressbarsStatusforms.aspx)

