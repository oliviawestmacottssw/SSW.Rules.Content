---
type: rule
title: Do you use predictive-textboxes instead of normal combo or text boxes?
uri: do-you-use-predictive-textboxes-instead-of-normal-combo-or-text-boxes
created: 2014-12-12T19:47:18.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 ​When getting users to choose data from a medium-long list, or to enter data that<br>                    has been predefined (such as Country names), it is a good idea to use a predictive-text<br>                    combos rather than normal combo or text boxes. A good implementation of predictive-text<br>                    combos will also perform a type-ahead affect, providing the user with a richer experience.
 
Also, predictive textboxes can be used with validation, or without. In instances where you don't mind if users add data to your collection you can turn validation off; however, to keep your collection clean, it is recommended to use validation.
![Incorrect use of data entry tools](/PublishingImages/PredTextBad.gif) Figure: Bad Example - Using a Textbox and Combo to enter list data![Good Example of predictive textboxes](/PublishingImages/TypeAhead.gif) Figure: Good Example - Predictive-Text combo with Type Ahead![Good Example of predictive textboxes](/PublishingImages/PredTextValidation.gif) Figure: Good Example - Predictive-Text combo with and without validation
To see this in action try our Predictive-Text Combos demo.

The predictive-text combo control used in our demo can be found on     [The Code Project](http&#58;//www.codeproject.com/) under the ASP.NET Controls Section listed as     [ComboBox Control for ASP.NET](http&#58;//www.codeproject.com/Articles/10504/ComboBox-Control-for-ASP-NET).

[DBCombo.Net](http&#58;//dbcombo.net/) is another predictive-text box written in .NET that allows users to type in what they are looking for and then provides a     [Google Suggest](https&#58;//www.google.com/) style drop down showing the matching results.

