---
type: rule
title: Do you use field and list item validation (in 2010)
uri: do-you-use-field-and-list-item-validation-in-2010
created: 2009-12-10T02:23:00.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

class CreateShoppingListHandler : SPItemEventReceiver
<br>    {
<br>        public override void ItemAdding(SPItemEventProperties properties)
<br>        {
<br>            float price = 0;
<br>            float cost = 0;

<br>            if(float.TryParse(properties.ListItem.Fields["Price"].ToString(), out price) && float.TryParse(properties.ListItem.Fields["Cost"].ToString(), out cost))
<br>            {
<br>                if(price < cost)
<br>                {
<br>                    properties.ErrorMessage = "The cost must not be less than the price";
<br>                    properties.Cancel = true;
<br>                }
<br>            }            
<br>        }
<br>    }Bad example: using custom code – creating a<br>custom event receiver on the item (the item adding event or item updating<br>event)
![](ListValidation.jpg)
Good example: using no code – just using the<br>field validation on a list
<br>A demo of this from Andrew Connell on
http://channel9.msdn.com/learn/courses/SharePoint2010Developer/ListsAndSchemas/FieldandListItemValidation/
