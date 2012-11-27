---
type: rule
title: Controls - Do you extend the size of your ComboBoxes to show as many results as possible? (Windows Forms Only)
uri: controls---do-you-extend-the-size-of-your-comboboxes-to-show-as-many-results-as-possible-windows-forms-only
created: 2012-11-27T09:20:17.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
When designing your form, it's a good idea to help your user whenever it's possible. So it's a good idea to extend your ComboBoxes to show as many results as possible to save your user from scrolling. Also, you should extend the width of the dropdown in order to show the longest items.
   ​
However, you should not extend your ComboBox without limit, normally the maximum number of items should be under 10 and the maximum width of the drop-down should be smaller than your hosting form.
![Options Form - ComboBox with text cut off](http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/ComboBox-Size-1.jpg)Figure: Bad Example - You have to scroll to see all the result, and the long results are cut off![Options Form - ComboBox with Extended Height and Width](http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/ComboBox-Size-2.jpg)Figure: Good Example - The size of the drop down has been extended to allow user to see as much as possible
Changing the maximum items is easy, just include the following code in your form:


```
cbxOUList.MaxDropDownItems = cbxOUList.Items.Count;
```


Changing the drop down size is a bit of tricky


```
Graphics g = Graphics.FromHwnd(this.Handle);
            SizeF stringSize = new SizeF();
            stringSize = g.MeasureString(longString, cbx.Font, 600);
            int adjustedSize = cbx.DropDownWidth;
            if ( adjustedSize<(int)stringSize.Width )
            {
               adjustedSize = (int)stringSize.Width;
            }
            cbx.DropDownWidth = adjustedSize;
```


