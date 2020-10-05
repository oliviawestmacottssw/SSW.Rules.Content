---
type: rule
title: Do you use a helper extension method to raise events?
uri: do-you-use-a-helper-extension-method-to-raise-events
created: 2018-04-30T21:21:26.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Enter Intro Text
 
Instead of:

private void RaiseUpdateOnExistingLotReceived()
{
if (ExistingLotUpdated != null)
{
ExistingLotUpdated();
}
}​

...use this event extension method:

public static void Raise&lt;t&gt;(this EventHandler&lt;t&gt; @event,
object sender, T args) where T : EventArgs
{
var temp = @event;
if (temp != null)
{
temp(sender, args);
}
}
public static void Raise(this Action @event)
{
var temp = @event;
if (temp != null)
{
temp();
}
}

That means that instead of calling:

RaiseExistingLotUpdated();

...you can do:

ExistingLotUpdated.Raise();

Less code = less code to maintain = less code to be blamed for ;)​
