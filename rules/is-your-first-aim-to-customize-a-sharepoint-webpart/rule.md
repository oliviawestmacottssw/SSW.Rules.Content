---
type: rule
archivedreason: 
title: Is your first aim to customize a SharePoint webpart?
guid: 8b78be7a-6ce0-4391-b4be-8650f0a0ba4d
uri: is-your-first-aim-to-customize-a-sharepoint-webpart
created: 2009-02-28T09:14:44.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: John Liu
  url: https://ssw.com.au/people/john-liu
related: []
redirects: []

---


This field should not be null (Remove me when you edit this field).
<br><excerpt class='endintro'></excerpt><br>
<p>These are some of the fields in the CQWP that are often configured&#58;</p>
<p><strong>MainXslLink, ItemXslLink&#58;</strong></p>
<p>These two controls the main and item XSL file paths.&#160; Set these to your new XSL file under /Style Library/XSL Style Sheets/SSW/SSWMainContent.xsl and SSWItem.xsl files</p>
<p><strong>ItemLimit </strong></p>
<p>The default number of items that are displayed on a Content Query web part is 15.&#160; With unlimited pages.&#160; Sometimes you want this number to be a lot higher (or -1 for no limit).</p>
<p>Note&#58; If you do make this unlimited - make sure your page is designed to grow infinitely or the layout may look strange.</p>
<p><strong>CommonViewFields </strong></p>
<p>The Content Query web part automatically selects a few of the common fields for any query.&#160; But sometimes you want a particular field that isn't selected by default.&#160; This is when you should use CommonViewFields.</p>
<p>The syntax is &quot;fieldname,fieldtype;&quot;</p>
<p>E.g. PublishingContent,PublishingHTML;</p>
<p><strong>Query and QueryOverride </strong></p>
<p>The Content Query web part gives the user a lot of flexibility to design the query in the UI toolpart.&#160; However if your needs are perculiar you can use the QueryOverride to skip over defining the query and use your supplied CAML directly.</p>
<p>
<dl class="badCode">
<dt><pre>[Guid(&quot;5bbdb385-5076-4a4b-85e8-691664b7f575&quot;)]<br> public class WebPart1 &#58; System.Web.UI.WebControls.WebParts.WebPart<br>&#123;<br>    public WebPart1() &#123; &#125;<br>    protected override void CreateChildControls()<br>    &#123;<br>        base.CreateChildControls();<br>        // TODO&#58; add custom rendering code here.<br>        Label label = new Label();<br>        label.Text = &quot;Hello World&quot;;<br>        this.Controls.Add(label);<br>    &#125;<br>&#125;<br></pre></dt>
<dd>Bad Example&#58; Inherit from System.Web.UI.WebControls.WebParts.WebPart</dd></dl>
<p></p>
<p>
<dl class="goodCode">
<dt><pre>public class RelatedContentByQueryWebPart&#58;CustomContentByQueryWebPart<br>&#123;<br>    public string RulesKeyWords //get the column name from SharePoint<br>    &#123;<br>        get;<br>        set;<br>    &#125;<br>    protected override void OverrideQuery()<br>    &#123;<br>        StringBuilder query = new StringBuilder();<br>        SPListItem item = SPContext.Current.ListItem;<br>        string[] rulesKeyWords = &#123;&#125;;<br>        if (item != null)<br>        &#123;<br>            ......<br>        &#125;<br>        this.QueryOverride = query.ToString(); // pass the query<br>    &#125;<br>&#125;<br></pre></dt>
<dd>Good Example&#58; Inherit from CustomContentByQueryWebPart</dd></dl>
<p></p>


