---
type: rule
archivedreason: 
title: Comments - Do you enforce comments with check-ins?
guid: 38313df6-15aa-448a-b978-edc43b582694
uri: comments-do-you-enforce-comments-with-check-ins
created: 2011-11-18T03:52:40.0000000Z
authors:
- title: David Klein
  url: https://ssw.com.au/people/david-klein
- title: Justin King
  url: https://ssw.com.au/people/justin-king
- title: Ryan Tee
  url: https://ssw.com.au/people/ryan-tee
- title: Tristan Kurniawan
  url: https://ssw.com.au/people/tristan-kurniawan
- title: Drew Robson
  url: https://ssw.com.au/people/drew-robson
related: []
redirects: []

---


This field should not be null (Remove me when you edit this field).
<br><excerpt class='endintro'></excerpt><br>

  <img alt="" class="ms-rteCustom-ImageArea" src="/TFS/RulesToBetterVersionControlwithTFS(AKASourceControl)/PublishingImages/CommentsBad.jpg" />&#160;<font class="ms-rteCustom-FigureBad" size="+0">Figure&#58; Bad Example&#58; No Comments against the check-ins we don’t know what changes were made in each revision </font><img alt="" class="ms-rteCustom-ImageArea" src="/TFS/RulesToBetterVersionControlwithTFS(AKASourceControl)/PublishingImages/CommentsGood.jpg" /> <font class="ms-rteCustom-FigureGood" size="+0">Figure&#58; Good Example&#58; Now we can pin point which revision a particular change has been made </font>
<p>More Information <br>
To enforce this behaviour, you will need to&#58; </p>
<ol>
    <li>Install Team Foundation Server Power Tools </li>
    <li>Right click the Team Project in Team Explorer &gt; Team Project Settings &gt; Source Control <img alt="" class="ms-rteCustom-ImageArea" src="/TFS/RulesToBetterVersionControlwithTFS(AKASourceControl)/PublishingImages/Enforce1.jpg" /> </li>
    <li>Select the Check-in Policy tab</li>
    <li>Click Add </li>
    <li>Select the Changeset Comments Policy <br>
    <img alt="" class="ms-rteCustom-ImageArea" src="/TFS/RulesToBetterVersionControlwithTFS(AKASourceControl)/PublishingImages/Enforce2.jpg" /> </li>
</ol>
Now the next time someone checks-in some code, they are forced to enter a comment.



