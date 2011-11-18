---
type: rule
title: Do you know to delete workspaces older than 6 months and warn on 3?
uri: do-you-know-to-delete-workspaces-older-than-6-months-and-warn-on-3
created: 2011-11-18T03:52:39.0000000Z
authors:
- id: 22
  title: David Klein
- id: 5
  title: Justin King
- id: 17
  title: Ryan Tee
- id: 6
  title: Tristan Kurniawan

---

 This field should not be null (Remove me when you edit this field). 
If a developer had code checked out to a workspace that they have not even looked at in months, what is the likelihood that they even remember what changes they were making?

Why do workspaces build up?- Developers use multiple computers
- Developers use volatile virtual computers
- Developers reinstall their workstation
- Developers get new workstations
- Developers leave


Developer checklist:- Check workspaces often to see what you don't need
- Delete any workspaces you no longer need


TFS Master Checklist:- Delete all workspaces that have not been edited in 6 months
- Warn developers for workspaces that have not been accessed in 3 months

![Longtime Workspaces](/TFS/RulesToBetterVersionControlwithTFS(AKASourceControl)/PublishingImages/LongtimeWorkspaces.jpg)Figure: Bad example - Rebecca has a workspace that has not been accessed in a while ![Current Workspaces](/TFS/RulesToBetterVersionControlwithTFS(AKASourceControl)/PublishingImages/CurrentWorkspaces.jpg)Figure: Good example - All of Julian's workspaces are current 
1. Open VS 2010, File | Source Control | WorkSpaces, click the "Show remote workspaces": ![Manage Workspaces ](/TFS/RulesToBetterVersionControlwithTFS(AKASourceControl)/PublishingImages/ManageWorkspaces.jpg)Figure: Manage Workspaces
2. Keep press "Ctrl", select the workspaces which haven't been used for a long time.
3. Click "Remove" button.


