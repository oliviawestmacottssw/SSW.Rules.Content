---
type: rule
title: Do you avoid "UI" in event names?
uri: do-you-avoid-ui-in-event-names
created: 2018-04-30T21:07:59.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

No "UI" in event names, the event raiser should be unaware of the UI in MVVM and user controls
The handler of the event should then do something on the UI. 
 
private void RaiseUIUpdateBidButtonsRed()
{
if (UIUpdateBidButtonsRed != null)
{
UIUpdateBidButtonsRed();
}
}
 Bad Code: Avoid "UI" in event names, an event is UI un-aware


private void RaiseSelectedLotUpdated()
{
if (SelectedLotUpdated != null)
{
SelectedLotUpdated();
}
}
 Good Code: We received an update on the currently selected item, change the UI correspondingly (or even better: use MVVM and data binding)
