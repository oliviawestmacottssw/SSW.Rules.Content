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

 ​By default WordPress shows the whole article content on a post list. Knowing that some posts are quite long - taking a lot of real estate on the page - it's a good idea to summarize it and add a "read more" link.​  
You can split your blog entries so that only the first part of certain posts is displayed on the home and archive pages. When you do this, a link will be placed after the intro, pointing the reader to the full post.
 To do so, you can either edit the source index.php (or similar) file; or just click the "Read More" tag button in the first ​row of the visual editor toolbar (or press  **Alt+Shift+T**):  

replace <br>      **&lt;?php the\_content(); ?&gt;** with <br>      **&lt;?php ****the\_excerpt();**** ?&gt;**Figure: Bad example - changing source php files is complicated​ and require developer skills​![](/PublishingImages/readmore-tag.png)Figure: Good example - click on the "Read More" tag on the post visual editor
**Note:** This is out-of-the-box with WordPress. You won't need a plugin.

### Custom Read More Message

To customize the message, simply add a space after     ** &lt;!--more** and insert the text you want to show:

&lt;!--more           Read the full post​--&gt;
Figure: Custom "read more" link
### Some WordPress themes do this automatically

Many WordPress themes will have an option to not show the full blog content on the homepage. E.g. in Avada (one of the most popular themes) it has this:
![excerpt.png](/PublishingImages/excerpt.png)Figure: Many WordPress themes makes it​ easier to you


Always check theme options before going back through posts to add in the Read More tags manually.

