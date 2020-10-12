---
type: rule
title: Do you initialize variables outside of the try block?
uri: do-you-initialize-variables-outside-of-the-try-block
created: 2018-04-26T21:41:56.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

You should initialize variables outside of the try block.
  
Cursor cur;
try
{
...
cur = Cursor.Current; //Bad Code - initializing the variable inside the try block
Cursor.Current = Cursors.WaitCursor;
...
}
finally
{
Cursor.Current = cur;
}
 Bad Example: Because of the initializing code inside the try block. If it failed on this line then you will get a NullReferenceException in Finally

Cursor cur = Cursor.Current; //Good Code - initializing the variable outside the try block
try
{
...
Cursor.Current = Cursors.WaitCursor;
...
}
finally
{
Cursor.Current = cur;
}
Good Example : Because the initializing code is outside the try block
