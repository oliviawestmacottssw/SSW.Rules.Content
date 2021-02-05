---
type: rule
archivedreason: 
title: Do you know your migration choices?
guid: acd96e8e-9cac-47ce-bdf8-865d5c383e7e
uri: do-you-know-your-migration-choices1
created: 2015-08-12T15:26:07.0000000Z
authors: []
related: []
redirects:
- do-you-know-your-migration-choices

---


<p><span style="line-height&#58;20.7999992370605px;">There are two main ways to move from TFS 2013 Update 4 to TFS 2015&#58;</span></p>
<br><excerpt class='endintro'></excerpt><br>
<p><strong>Option 1&#58; </strong><strong>In-place migration (Recommended)</strong></p><p>With an in-place migration, you essentially install TFS 2015 over the top of an existing TFS 2013 Update 4 installation. The benefits of this approach are that you don't need additional hardware, and don't need to change network settings like DNS addresses to change between environments.</p><p>&#160;</p><p><strong>Option 2&#58; Migration to a new environment</strong></p><p>Migrating to a new environment may be required if you need to move to new upgraded hardware, or if you are not confident with your rollback plan. The key benefit with migrating to a new environment is that you can quickly switch back to your original environment should anything go wrong during the upgrade.</p><p>&#160;</p><p><strong>Reducing downtime</strong></p><p>With both options, you can also use the <a href="https&#58;//msdn.microsoft.com/en-us/Library/vs/alm/TFS/upgrade/pre-upgrade">TfsPreUpgrade tool to reduce downtime</a>. As per the article, the TfsPreUpgrade tool will&#58;</p><ul style="list-style-type&#58;disc;"><li>Enable compression for a small number of tables that were not compressed in 2013 but will be in 2015.</li><li>Scan for and fix a very rare but well understood data corruption in TFS version control data.</li><li>Create new tables and migrate existing data to them.</li><li>Create triggers.</li><li>Update stored procedures.</li><li>Create indexes.</li></ul><p>By using the TfsPreUpgrade tool, you can thereby reduce the downtime for the actual cut-over to the new version by ensuring that your databases are updated in advance.</p>


