---
type: rule
title: Do you always use the html maxlength attribute on input fields to limit number of characters to the length of the field in the table?
uri: do-you-always-use-the-html-maxlength-attribute-on-input-fields-to-limit-number-of-characters-to-the-length-of-the-field-in-the-table
created: 2016-08-24T21:56:21.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

**Rule 1: ** Whenever you have a data entry page you should always use the html maxlength attribute to limit number of characters to the length of the field in the table (except for numbers).

**Rule 2:**  Whenever you have a situation where you are using the HTML textarea (does not have the maxlength property)
 
Then you need to:

- add the JavaScript function eg. ValidateLength(control)
- add 2 properties to every data control  eg. dataType="char" onkeyup="validateLength(this)"
