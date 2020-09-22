---
type: rule
title: Do you provide a warning before the program exits?
uri: do-you-provide-a-warning-before-the-program-exits
created: 2012-11-27T03:10:56.0000000Z
authors: []

---

 
​A product should not close without providing a warning. We use the following message box to warn the user before closing a program:
   ​![SSW Exchange Reporter - Are you sure you want to exit?](../../assets/CloseWarning.gif)Figure: Good Example - Standard warning before a program exits

```
private void OnExit(object sender) 
             { 
                EventHandler handler = ExitRequest; 
                if (handler!= null ) 
                { 
                   handler(sender, EventArgs.Empty);
                   return;
                } 
                string closeTitle = string.Format("Exiting{0}", Application.ProductName);
                string closeMessage = string.Format("Are you sure you want to exit {0}", Application.ProductName);
                DialogResult result = MessageBox.Show(closeMessage,closeTitle, MessageBoxButtons.YesNo,MessageBoxIcon.Warning);
                if (result == DialogResult.Yes)
                { 
                   Application.Exit();
                } 
             }
```


We have an example of this in the [SSW .NET Toolkit](http://www.ssw.com.au/ssw/NETToolkit/).

