---
type: rule
title: Do you format "Environment.NewLine" at the end of a line?
uri: do-you-format-environmentnewline-at-the-end-of-a-line
created: 2018-04-26T21:46:51.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

You should format "Environment.NewLine" at the end of a line.​​
​
 
string message = "The database is not valid." + Environment.NewLine + "Do you want to upgrade it? ";
Bad Example: "Environment.NewLine" isn't at the end of the line 



string message = "The database is not valid." + Environment.NewLine;
message += "Do you want to upgrade it? ";​
Good Example:  "Environment.NewLine" is at the end of the line 

​​

return string.Join(Environment.NewLine, paragraphs);
Good Example: ​"Environment.NewLine" is an exception for String.Join  
​
