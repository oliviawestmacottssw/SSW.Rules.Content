---
type: rule
archivedreason: 
title: Do you use version control with Power BI?
guid: 80cbeca6-d33a-4ad3-8127-d3ae46fc5f00
uri: do-you-use-version-control-with-power-bi
created: 2017-03-29T06:06:12.0000000Z
authors:
- title: Mehmet Ozdemir
  url: https://ssw.com.au/people/mehmet-ozdemir
- title: Patricia Barros
  url: https://ssw.com.au/people/patricia-barros
- title: Chris Beaver
  url: https://ssw.com.au/people/chris-beaver
related:
- do-you-know-the-best-tool-to-migration-from-tfvc-to-git
redirects: []

---


To save your Power BI files in source control, you need to&#58;<br>
<br><excerpt class='endintro'></excerpt><br>
<p></p>​​Prior to the April 2016 update, storing a Power BI Report in version control was often prohibitive, as the pbix file contains the datasets along with the report definitions, which in some cases can be gigabytes in size.<br>The April 2016 update features the ability to export a Power BI Report Template File (pbit), which contains the report definition minus the dataset, making it much simpler to keep track of changes in your favourite source control application.<br>To export the template from Power BI Desktop, select File | Export | Power BI template from the menu, enter a description, file name and click save, as per the below figures.<br>&lt;img src=”https&#58;//rules.ssw.com.au/PublishingImages/PowerBI-SourceControl-1-3.jpg&quot;&gt;<br><strong>Figure&#58; Exporting a Power BI Template from Power BI Desktop</strong><br>​&lt;img src=”https&#58;//rules.ssw.com.au/PublishingImages/PowerBI-SourceControl-2-3.jpg&quot;&gt;<br><strong>Figure&#58; Enter a Description for the Template</strong><br>&lt;img src=”https&#58;//rules.ssw.com.au/PublishingImages/PowerBI-SourceControl-3-3.jpg&quot;&gt;<br><strong>Figure&#58; Enter a File Name and Save</strong><br>Save your pbix file to the same folder as the template above, you’ll need these if you want to publish your report to Power BI Online. &#160;Make sure your source control is configured to ignore *.pbix files, otherwise you’ll be saving data in source control!<br>


