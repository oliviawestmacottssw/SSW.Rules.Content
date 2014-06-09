---
type: rule
title: Do you use 'read more' WordPress tag to show summary only on a blog list?
uri: do-you-use-read-more-wordpress-tag-to-show-summary-only-on-a-blog-list
created: 2014-06-09T15:12:04.0000000Z
authors:
- id: 16
  title: Tiago Araujo
- id: 1
  title: Adam Cogan

---

 By default WordPress shows the whole article content on a post list. Knowing that some posts are quite long - taking a lot of real estate on the page - it's a good idea to summarize it and add a "read more" link.​  
You can easily split your blog entries so that only the first part of certain posts is displayed on the home and archive pages. When you do this, a link will be placed after the intro, pointing the reader to the full post. To do so, find the "Read More" tag button in the first ​row of the visual editor toolbar or press     **Alt+Shift+T**:
![](/WebSites/RulesToBetterWordPress/PublishingImages/readmore-tag.png)Figure: Good example - click on the "Read More" tag on the post visual editor
### Custom Read More Message
 To customize the message, simply add a space after     ** &lt;!--more** and insert the text you want to show:     
&lt;!--more              Read the full post​--&gt;
Figure: Custom "read more" link​
It can also be done it in the hard way, by editing the source index.php (or similar) file.​
replace &lt;?php the\_content(); ?&gt; with &lt;?php the\_excerpt(); ?&gt;Figure: Bad example - changing source php files​
