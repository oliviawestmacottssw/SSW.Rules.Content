---
type: rule
archivedreason: 
title: Do you use 'read more' WordPress tag to show summary only on a blog list?
guid: 18e3c2af-0fc0-4e83-9afd-f8a6c1b60e56
uri: do-you-use-read-more-wordpress-tag-to-show-summary-only-on-a-blog-list
created: 2014-06-09T15:12:04.0000000Z
authors:
- title: Tiago Araujo
  url: https://ssw.com.au/people/tiago-araujo
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


By default WordPress shows the whole article content on a post list. Knowing that some posts are quite long - taking a lot of real estate on the page - it's a good idea to summarize it and add a &quot;read more&quot; link.​ 
<br><excerpt class='endintro'></excerpt><br>
<p>You can split your blog entries so that only the first part of certain posts is displayed on the home and archive pages. When you do this, a link will be placed after the intro, pointing the reader to the full post.</p>

To do so, you can either edit the source index.php (or similar) file; or just click the &quot;Read More&quot; tag button in the first ​row of the visual editor toolbar (or press <strong>Alt+Shift+T</strong>)&#58; <p></p><dl class="badImage"><dt class="greyBox">replace <strong>&lt;?php the_content(); ?&gt;</strong> with <strong>&lt;?php&#160;</strong><span class="ssw15-rteStyle-Highlight"><strong>the_excerpt();</strong></span><strong>&#160;?&gt;</strong></dt><dd>Figure&#58; Bad example - changing source php files is complicated​ and require developer skills​</dd></dl><dl class="goodImage"><dt> 
      <img src="/WebSites/RulesToBetterWordPress/PublishingImages/readmore-tag.png" alt="" /> 
   </dt><dd>Figure&#58; Good example - click on the &quot;Read More&quot; tag on the post visual editor</dd></dl><h3>Custom Read More Message</h3> To customize the message, simply add a space after 
<strong> &lt;!--more</strong> and insert the text you want to show&#58; 
<dl class="image"><dt class="greyBox"><p>&lt;!--more 
         <span class="ssw15-rteStyle-Highlight">Read the full post​</span>--&gt;</p></dt><dd>Figure&#58; Custom &quot;read more&quot; link</dd></dl>​



