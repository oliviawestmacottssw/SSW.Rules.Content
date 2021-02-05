---
type: rule
archivedreason: 
title: Do You Help Users By Selecting A Default Field
guid: 052a145d-827a-435d-afb7-d80911e36266
uri: do-you-help-users-by-selecting-a-default-field
created: 2012-04-19T04:31:18.0000000Z
authors: []
related: []
redirects: []

---


​Help your users by setting the default field when your MVC WebSite loads.​​
<br><excerpt class='endintro'></excerpt><br>
<div>By selecting a default field for your users when a page loads&#160;you can improve the usability of your web site by reducing the amount of steps needed to perform a&#160;task.</div>
<div><br></div>
<div>Here is a&#160;way&#160;to do this with&#160;MVC 3 and&#160;Razor&#58;</div>
<div>1.&#160;Add a div with a class around the field you want to set focus on</div>
<div><br></div>
<blockquote style="margin&#58;0px 0px 0px 40px;border-style&#58;none;padding&#58;0px;"><pre style="color&#58;rgb(0, 0, 0);background-color&#58;rgb(255, 255, 255);"><span style="color&#58;rgb(128, 128, 48);">&lt;</span>div <span style="color&#58;rgb(128, 0, 0);font-weight&#58;bold;">class</span><span style="color&#58;rgb(128, 128, 48);">=</span><span style="color&#58;rgb(128, 0, 0);">&quot;</span><span style="color&#58;rgb(0, 0, 230);">focus</span><span style="color&#58;rgb(128, 0, 0);">&quot;</span><span style="color&#58;rgb(128, 128, 48);">&gt;</span></pre>
<pre style="background-color&#58;rgb(255, 255, 255);">    @Html<span style="color&#58;rgb(128, 128, 48);">.</span><font color="#000000">EditorFor</font><font color="#000000"></font><span style="color&#58;rgb(128, 128, 48);">(</span><font color="#000000">model </font><span style="color&#58;rgb(128, 128, 48);">=</span><span style="color&#58;rgb(128, 128, 48);">&gt;</span><font color="#000000"> </font><font color="#000000">model</font><span style="color&#58;rgb(128, 128, 48);">.</span><font color="#000000">FirstName</font><font color="#000000"></font><span style="color&#58;rgb(128, 128, 48);">)</span><font color="#000000">​
    @Html</font></pre>
<pre style="background-color&#58;rgb(255, 255, 255);"><font color="#000000">    @</font><font color="#000000">Html</font><span style="color&#58;rgb(128, 128, 48);">.</span><font color="#000000">ValidationMessageFor</font><font color="#000000"></font><span style="color&#58;rgb(128, 128, 48);">(</span><font color="#000000">model </font><span style="color&#58;rgb(128, 128, 48);">=</span><span style="color&#58;rgb(128, 128, 48);">&gt;</span><font color="#000000"> </font><font color="#000000">model</font><span style="color&#58;rgb(128, 128, 48);">.</span><font color="#000000">FirstName</font><font color="#000000"></font><span style="color&#58;rgb(128, 128, 48);">)</span></pre>
<pre style="background-color&#58;rgb(255, 255, 255);"><span style="color&#58;rgb(128, 128, 48);">&lt;</span><span style="color&#58;rgb(128, 128, 48);">/</span><font color="#000000">div</font><span style="color&#58;rgb(128, 128, 48);">&gt;</span></pre></blockquote>
<div><div><br></div>
<div>2. Then use jQuery to select the class and set focus​&#58;</div></div>
<div><br></div>
<blockquote style="margin&#58;0px 0px 0px 40px;border-style&#58;none;padding&#58;0px;"><pre style="color&#58;rgb(0, 0, 0);background-color&#58;rgb(255, 255, 255);">$<span style="color&#58;rgb(128, 128, 48);">(</span><span style="color&#58;rgb(128, 0, 0);font-weight&#58;bold;">function</span><span style="color&#58;rgb(128, 128, 48);">(</span><span style="color&#58;rgb(128, 128, 48);">)</span> <span style="color&#58;rgb(128, 0, 128);">&#123;</span></pre>
<pre style="color&#58;rgb(0, 0, 0);background-color&#58;rgb(255, 255, 255);">    $<span style="color&#58;rgb(128, 128, 48);">(</span><span style="color&#58;rgb(0, 0, 230);">'.focus &#58;input'</span><span style="color&#58;rgb(128, 128, 48);">)</span><span style="color&#58;rgb(128, 128, 48);">.</span>focus<span style="color&#58;rgb(128, 128, 48);">(</span><span style="color&#58;rgb(128, 128, 48);">)</span><span style="color&#58;rgb(128, 0, 128);">;</span></pre>
<pre style="color&#58;rgb(0, 0, 0);background-color&#58;rgb(255, 255, 255);"><span style="color&#58;rgb(128, 0, 128);">&#125;</span><span style="color&#58;rgb(128, 128, 48);">)</span><span style="color&#58;rgb(128, 0, 128);">;</span></pre></blockquote>


