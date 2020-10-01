---
type: rule
title: Form Design - Do you change contact method options from default option group to checkboxes?
uri: form-design---do-you-change-contact-method-options-from-default-option-group-to-checkboxes
created: 2012-12-10T19:31:39.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

![ Bad Example - By default CRM uses option group for contact's and account's<br>            contact methods.](CRMContactMethods.jpg)            
As per our rule [Do you know when to use CheckBox?](http://www.ssw.com.au/SSW/standards/rules/RulesToBetterInterfacesEdit.aspx#UseCheckBox). Checkboxes should be used instead of the           option group since the answer is a boolean type. You can change the option group           to checkboxes by:

1. From CRM, go to Settings | Customizations | Customize Entities
2. Double-Click "Contact" entity
3. Click "Form and Views"
4. Double-Click "Form" to edit contact form
5. Click "Administration" tab
6. Select a contact method field, i.e. Email
7. Click "Change Properties"<br>            ![ Select and change the email field's properties.](CRMChangeContactMethodsFieldProperties.jpg)                
8. Click "Formatting" tab
9. Change layout from "Two Columns" to "One Column" and select "Check box" as control<br>            formatting
![ Change layout and control formatting of email field to one column type and<br>              check box.10. Repeat steps 6-9 for other contact method](CRMChangeContactMethodsFieldProperties.jpg)              
11. Repeat steps 3-9 for account entity

[[goodExample]]
| ![Checkboxes are used for contact methods because they're clear<br>            and simple.](CRMContactMethodsWithCheckboxes.jpg)
