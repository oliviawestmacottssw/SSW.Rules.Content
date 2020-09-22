---
type: rule
title: Do you clean useless calendars in SharePoint?
uri: do-you-clean-useless-calendars-in-sharepoint
created: 2013-09-05T23:49:53.0000000Z
authors:
- id: 9
  title: William Yin
- id: 34
  title: Brendan Richards

---

 Most SharePoint site templates contain a calendar list, this will bring lots of useless calendars.

 
​Use the below PowerShell script to clean them:​​

$site = Get-SPSite("http:///"); # Specify url here​
​foreach ($web in $site.AllWebs) {    ​
    $lists = $web.Lists
    for ($i=($lists.Count-1);$i -gt 0; $i--) {  
        $list = $lists[$i]
        #Write-host $i  $list.Title $list.BaseTemplate.ToString()
        if ($list.BaseTemplate.ToString().ToLower().contains('events')) {      
            if ($list.Items.Count -eq 0)
            {​
                Write-Host $list.Items.Count "items in the list" $list.Title '('$list.BaseTemplate') at '$web.Url "- cleaning it!"
                $list.Recycle()
                #$list.Delete()
            }
        }
    }
}  ​

This script will put the calendars which do not have any events into **Site Settings** | **Recycle Bin**:
​![EmptyCalendarsInRecyckeBin.png](EmptyCalendarsInRecyckeBin.png)​Figure: Empty Calendars in Recycle Bin folder
​

