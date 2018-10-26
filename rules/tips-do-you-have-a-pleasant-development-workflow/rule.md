---
type: rule
archivedreason: 
title: Tips - Do you have a pleasant development workflow?
guid: 8a51eaf0-0c2e-4fc5-8772-52c0082e772a
uri: tips-do-you-have-a-pleasant-development-workflow
created: 2016-04-22T22:24:13.0000000Z
authors:
- title: Steve Leigh
  url: https://ssw.com.au/people/steve-leigh
- title: Gabriel George
  url: https://ssw.com.au/people/gabriel-george
related: []
redirects: []

---


<p class="ssw15-rteElement-InfoBox"><b>UPDATE&#58; </b>This rule is irrelevant because Angular CLI provides a pleasant development workflow. Using ng serve, TypeScript transpilation occurs automatically and quickly (almost instantly).</p><p>When dealing with client-side development – especially when transpiling TypeScript – it is common to have to wait for several seconds between writing code, and seeing the results.<br></p><p>This adds up quickly – if you have to wait for 5 seconds every 3 minutes, you've spent 13 minutes of your day just <em>waiting</em>. This is a conservative estimate - we change code much more frequently than every 3 minutes!</p>
<br><excerpt class='endintro'></excerpt><br>
<p>A naïve development experience is as follows&#58;</p><div class="greyBox"><ol><li>Make a code change using a misconfigured IDE<ul><li>See errors everywhere as you type (even though the code is perfectly fine)</li><li>Inaccurate IntelliSense information</li></ul></li><li>Compile the code<ul><li>Since the TypeScript compilation task is often part of the project build, this is a common way to recompile to JavaScript</li></ul></li><li>Run a gulp task to copy files around appropriately<ul><li>This often takes a few seconds to run, especially if it “cleans” the folder beforehand</li></ul></li><li>Refresh the page<ul><li>Depending on the setup, this may take anywhere from&#160;milliseconds to seconds</li></ul></li><li>Click around until the app is in the right state to test the functionality<ul><li>If there is too much built-up state, and no routes set up, this chews up time</li></ul></li></ol></div><div><dd class="ssw15-rteElement-FigureBad"> Bad example - Many hours each week are wasted just waiting for the code you wrote to run&#160;</dd><p><br></p><p>A more ideal workflow is&#58;<br></p><div class="greyBox"><ol><li>Make the change using a properly configured IDE<ul><li>One that only shows errors when they’re appropriate<br></li><li>Intellisense shows everything available, and nothing more</li></ul></li><li>Refresh the page (maybe)<ul><li>With well set up watches for compilation&#160;and appropriate use of BrowserLink or LiveReload, this is very fast</li><li>With proper bundling, the initial page load is also fast in development environments.</li></ul></li><li>Already be at the component required, ready to check it works</li></ol></div><dd class="ssw15-rteElement-FigureGood"> Good example - No time is wasted doing repetitive and slow tasks </dd><p> 
      <strong> <br></strong></p><p>
      <strong> Remember</strong>&#58; Spending 4 hours setting up a good dev experience will pay for itself within the week, and make your work like much happier.</p><h3>Guidelines to follow&#58;</h3><ul><li>Ensure that only the files that are changed need to be compiled – TypeScript handles this quite well with --watch</li><li>Avoid the use of task runners (eg. gulp) as part of your development flow. A few watches should be all you need. Save the task runners for release builds</li><li>Consider separate index pages for production and development, using the dev libraries for development, and minified/bundled ones for production</li><li>Use module loaders (eg. SystemJS) to manage dependencies&#160;and their associated bundlers/builders for releases</li><li>Load 3rd party modules (eg. Angular2 and Rx) as a bundle, not as their individual files – speed up development first-page load</li><li>Think about your routing – a refresh should almost always return the page to the exact same state or at the very least, the same screen</li><li>Most importantly, <strong>be unsatisfied</strong> - if things are slow, fix it. If you constantly have to manually close IISExpress to run your app, <em>find out why</em> and fix it! You will save everyone time in the long run​<br></li></ul>​</div>


