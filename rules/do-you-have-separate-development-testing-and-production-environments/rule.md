---
type: rule
title: Do you have separate development, testing and production environments?
uri: do-you-have-separate-development-testing-and-production-environments
created: 2009-03-10T07:02:13.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 This field should not be null (Remove me when you edit this field). 
The best solution is to use build scripts (.bat and .vbs files) to automatically create a setup package that can be used to deploy to testing and production environment. For backend changes, you can either include the change scripts with the setup package (if it's localised database), or run those scripts as part of your deployment process.

Read more about setup packages at [SSW's Wise Standard for Products.](http&#58;//www.ssw.com.au/ssw/Standards/wisesetup/WiseStandards.aspx)

**Now make each environment clear.**

Whenever an application has a database, have a visual indicator. I recommend a different background color for each environment

- Red for the **Development** database<br>
- Yellow for the **Test** database<br>
- Grey (no colour) for the **Production** database


Note: The Yellow might have been Orange (kind of like traffic lights) but the color palette in Word doesn't give Orange.
![colors in Word color pallete](/Standards/Management/RulesToSuccessfulProjects/PublishingImages/WordColorPallete.GIF)Figure: colors in Word color palette 
This prevents testers from accidentally entering test data into production version.

**Windows Forms Tip:** Implement in the base form in the header 
**ASP.NET 2.0 Tip:** Implement in the master form in the header
![ ](/Standards/Management/RulesToSuccessfulProjects/PublishingImages/dev_test_prod_servers.gif) Figure: Spice up your environments with different colors 
An application of this rule is how we identify our CRM servers - see rule [Do you identify Development, Test and Production CRM Web Servers by colors?](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulestoBetterMicrosoftCRM.aspx#Environment)

