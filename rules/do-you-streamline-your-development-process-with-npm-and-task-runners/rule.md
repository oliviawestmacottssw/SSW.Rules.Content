---
type: rule
archivedreason: 
title: Do you streamline your development process with NPM and Task Runners?
guid: 321b6beb-86c9-4df0-b200-f8a6a3aaf10a
uri: do-you-streamline-your-development-process-with-npm-and-task-runners
created: 2015-08-11T04:20:48.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Chris Briggs
  url: https://ssw.com.au/people/chris-briggs
related: []
redirects: []

---


<span><p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"><span style="font-size:14.6666666666667px;font-family:arial;color:#212121;vertical-align:baseline;white-space:pre-wrap;">​The current trend in web development is to use a large range of front-end libraries to give a great user experience.</span></p><p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"><span style="font-size:14.6666666666667px;font-family:arial;color:#212121;vertical-align:baseline;white-space:pre-wrap;"> </span></p><p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"><span style="font-size:14.6666666666667px;font-family:arial;color:#212121;vertical-align:baseline;white-space:pre-wrap;">However, .NET devs know it is no easy task to manage all of these on top of a large script folder. Previously we tried to improve and streamline the process by using NuGet, but found this package manager was ill-suited.</span><span style="color:#000000;font-family:'times new roman';font-size:16px;white-space:pre-wrap;line-height:20px;background-color:transparent;"> </span></p><p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"><span style="color:#000000;font-family:'times new roman';font-size:16px;white-space:pre-wrap;line-height:20px;background-color:transparent;"><br></span></p><span><p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"><span style="font-size:14.6666666666667px;font-family:arial;color:#212121;vertical-align:baseline;white-space:pre-wrap;">Another issue was that due to the requirement of checking the library’s files into source control, this has the potential to grind fellow devs to a halt while Visual Studio tries to make sense of the myriad of small JavaScript files. Furthermore, there were many smaller tasks that needed to be completed, such as minification and bundling. In the older versions of Visual Studio, a large portion of these tasks had be performed manually by the developer.</span></p><p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"><span style="font-size:16px;font-family:'times new roman';color:#000000;vertical-align:baseline;white-space:pre-wrap;background-color:transparent;"> </span></p><span style="font-size:14.6666666666667px;font-family:arial;color:#212121;vertical-align:baseline;white-space:pre-wrap;">Needless to say, however a developer could try to tackle this task, it was always a challenging and time consuming endeavour.</span></span><p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"><span style="color:#000000;font-family:'times new roman';font-size:16px;white-space:pre-wrap;line-height:20px;background-color:transparent;"><br></span></p></span>
<br><excerpt class='endintro'></excerpt><br>
<span style="font-size:11pt;font-family:arial;"></span><span style="color:#212121;white-space:pre-wrap;line-height:1.38;font-size:11pt;font-family:arial;">Enter Visual Studio 2015 with NPM (Node Package Manager) in-built. This package manager has been built from the ground up to make downloading your JavaScript libraries simple. These tools existed outside of the .NET space, but in 2015 they’ve been brought into the fold and made easy to use in Visual Studio 2015. </span> 
<span style="font-size:11pt;font-family:arial;"> 
   <p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
      <span style="color:#212121;vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;"> </span></p> 
   <p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
      <span style="color:#212121;vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;">With NPM, we specify the name of the package and the version number we want to use, and the tool does all of the hard work finding and downloading the library. Because NPM is run on each developer’s machine, libraries are no longer added to source control. Rather, they are quickly downloaded from the trusted NPM CDN.</span></p> 
   <div> 
      <span style="color:#212121;vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;">
         <br></span></div> 
   <div> 
      <span style="font-size:11pt;font-family:arial;"> 
         <p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
            <span style="color:#212121;vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;">​<img src="../../assets/J6Na8pCSdsCvnIzhWHXLpbjtZd6Jp54rITnBd47JVS_7fDCcThur_Mwb3XmbCucETMHzGO7IGJFU3cUZZYJ1xr3-A_Rj9mzZkgXMWHD0B3hAWKS9gUXveakUU52HFdH_c8a2y8I.jpg" alt="bower json.png" style="margin:5px;" /></span> </p> 
         <p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
            <span style="color:#000000;font-weight:700;vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;">Figure: Example of NPM in action </span></p> 
         <p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
            <span style="color:#000000;vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;background-color:transparent;"> </span></p> 
         <p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
            <span style="font-size:11pt;font-family:arial;"> 
               <span style="color:#212121;vertical-align:baseline;white-space:pre-wrap;">Working in tandem with NPM are task runners, which a</span><span style="color:#333332;vertical-align:baseline;white-space:pre-wrap;">re JavaScript tools that can be used to add automation to your project by having them perform </span> 
               <span style="color:#212121;vertical-align:baseline;white-space:pre-wrap;">simple yet tedious tasks that are required to get your libraries ready for use, </span> 
               <span style="color:#333332;vertical-align:baseline;white-space:pre-wrap;">such as compilation, linting, and minification. Just use NPM to install the task runner of your choice, and away you go.</span></span></p> 
         <p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
            <span style="color:#333332;vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;"> </span></p> 
         <p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
            <span style="color:#333332;vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;">There are a heap of different task runners out there, the two best known are Gulp and Grunt.</span></p> 
         <p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
            <span style="color:#000000;vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;background-color:transparent;"> </span></p> 
         <p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
            <span style="color:#000000;vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;background-color:transparent;">
               
               <img src="../../assets/sJslIcCSh-m6MaqGaIfMaECtlFQKmQa8Nb5LyLH9HhUxFE-64TlBlmdmq551WXY1wJa9pcGwQd8aXG4fFM2fWy-0R3kqPmCZO09Y0HJ3HfRxp0VHOkpX7q-MkZ2sc3h91nFG5tw.jpg" width="624px;" alt="gulp vs grunt.png" height="239px;" style="margin:5px;" /></span> </p> 
         <p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
            <span style="color:#333332;font-weight:700;vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;">Figure: In short they both perform the same job but Gulp is faster and requires less configuration</span></p> 
         <p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
            <span style="color:#000000;font-weight:700;vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;background-color:transparent;"> </span></p> 
         <p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
            <span style="color:#212121;vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;">For example, we could previously use web essentials to do a lot of the necessary bundling and automation, but this was killed off at the start of 2015.</span></p> 
         <p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
            <span style="color:#212121;vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;">
               <img src="../../assets/yby2R29SDq_lu7nIv10InLfsVF4PNx4ISPoNm5RHCgVgC2ES5cwPm0oEj-nPPUIzWW47WHnsY4r4n_FVT69vKNAO34JV_ZhNyQX6rYd8-QlidccZ1tqwedf5ZuaST-cpW5yF3w8.jpg" width="624px;" alt="removed features.png" height="296px;" style="margin:5px;" /></span> </p> 
         <p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
            <span style="color:#000000;font-weight:700;vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;background-color:transparent;">Figure: The updated feature list for Web Essentials 2015</span></p> 
         <p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
            <span style="color:#000000;font-weight:700;vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;background-color:transparent;"> </span></p> 
         <p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
            <span style="color:#212121;vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;">This key feature was removed, but with the addition of tasks runners to Visual studio 2015 we can reimplement the functionality, by using ether Gulp or Grunt. For a number of reasons, Gulp is the better choice over Grunt: seen below is an example of a task for Gulp that will compile .less to .css</span></p> 
         <br> 
         <div dir="ltr" style="margin-left:0pt;"> 
            <span style="font-size:11pt;font-family:arial;"></span>
            <span style="font-size:11pt;font-family:arial;"></span>
            <span style="font-size:11pt;font-family:arial;"></span>
            <span style="font-size:11pt;font-family:arial;"></span>
            <span style="font-size:11pt;font-family:arial;"></span>
            <span style="font-size:11pt;font-family:arial;"></span>
            <span style="font-size:11pt;font-family:arial;"></span>
            <span style="font-size:11pt;font-family:arial;"></span>
            <span style="font-size:11pt;font-family:arial;"></span>
            <span style="font-size:11pt;font-family:arial;"></span>
            <span style="font-size:11pt;font-family:arial;"></span>
            <span style="font-size:11pt;font-family:arial;"></span>
            <span style="font-size:11pt;font-family:arial;"></span>
            <span style="font-size:11pt;font-family:arial;"></span> 
            <table style="border:none;"> 
               <colgroup>
                  <col width="22" />
                  <col width="399" /></colgroup> 
               <tbody><tr style="height:0px;"><td style="border:0px solid #000000;vertical-align:top;padding:4px 7px 7px;"> 
                        <br> 
                     </td><td style="border:0px solid #000000;vertical-align:top;padding:7px;"><p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
                           <span style="font-size:11pt;font-family:arial;">
                              <span style="color:#a71d5d;vertical-align:baseline;white-space:pre-wrap;">var</span><span style="vertical-align:baseline;white-space:pre-wrap;"> gulp </span> 
                              <span style="color:#a71d5d;vertical-align:baseline;white-space:pre-wrap;">=</span><span style="vertical-align:baseline;white-space:pre-wrap;"> </span> 
                              <span style="color:#0086b3;vertical-align:baseline;white-space:pre-wrap;">require</span><span style="vertical-align:baseline;white-space:pre-wrap;">(</span><span style="color:#183691;vertical-align:baseline;white-space:pre-wrap;">'gulp'</span><span style="vertical-align:baseline;white-space:pre-wrap;">);</span></span></p></td></tr><tr style="height:0px;"><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"> 
                        <br> 
                     </td><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"><p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
                           <span style="font-size:11pt;font-family:arial;">
                              <span style="color:#a71d5d;vertical-align:baseline;white-space:pre-wrap;">var</span><span style="vertical-align:baseline;white-space:pre-wrap;"> less </span> 
                              <span style="color:#a71d5d;vertical-align:baseline;white-space:pre-wrap;">=</span><span style="vertical-align:baseline;white-space:pre-wrap;"> </span> 
                              <span style="color:#0086b3;vertical-align:baseline;white-space:pre-wrap;">require</span><span style="vertical-align:baseline;white-space:pre-wrap;">(</span><span style="color:#183691;vertical-align:baseline;white-space:pre-wrap;">'gulp-less'</span><span style="vertical-align:baseline;white-space:pre-wrap;">);</span></span></p></td></tr><tr style="height:0px;"><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"> 
                        <br> 
                     </td><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"><p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
                           <span style="font-size:11pt;font-family:arial;">
                              <span style="color:#a71d5d;vertical-align:baseline;white-space:pre-wrap;">var</span><span style="vertical-align:baseline;white-space:pre-wrap;"> path </span> 
                              <span style="color:#a71d5d;vertical-align:baseline;white-space:pre-wrap;">=</span><span style="vertical-align:baseline;white-space:pre-wrap;"> </span> 
                              <span style="color:#0086b3;vertical-align:baseline;white-space:pre-wrap;">require</span><span style="vertical-align:baseline;white-space:pre-wrap;">(</span><span style="color:#183691;vertical-align:baseline;white-space:pre-wrap;">'path'</span><span style="vertical-align:baseline;white-space:pre-wrap;">);</span></span></p></td></tr><tr style="height:0px;"><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"> 
                        <br> 
                     </td><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"><p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
                           <span style="font-size:11pt;font-family:arial;">
                              <span style="color:#a71d5d;vertical-align:baseline;white-space:pre-wrap;">var</span><span style="vertical-align:baseline;white-space:pre-wrap;"> plumber </span> 
                              <span style="color:#a71d5d;vertical-align:baseline;white-space:pre-wrap;">=</span><span style="vertical-align:baseline;white-space:pre-wrap;"> </span> 
                              <span style="color:#0086b3;vertical-align:baseline;white-space:pre-wrap;">require</span><span style="vertical-align:baseline;white-space:pre-wrap;">(</span><span style="color:#183691;vertical-align:baseline;white-space:pre-wrap;">'gulp-plumber'</span><span style="vertical-align:baseline;white-space:pre-wrap;">);</span></span></p></td></tr><tr style="height:0px;"><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"> 
                        <br> 
                     </td><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"><p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
                           <span style="font-size:11pt;font-family:arial;">
                              <span style="vertical-align:baseline;white-space:pre-wrap;">gulp.task(</span><span style="color:#183691;vertical-align:baseline;white-space:pre-wrap;">'less'</span><span style="vertical-align:baseline;white-space:pre-wrap;">, </span> 
                              <span style="color:#a71d5d;vertical-align:baseline;white-space:pre-wrap;">function</span><span style="vertical-align:baseline;white-space:pre-wrap;"> () {</span></span></p></td></tr><tr style="height:0px;"><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"> 
                        <br> 
                     </td><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"><p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
                           <span style="font-size:11pt;font-family:arial;">
                              <span style="vertical-align:baseline;white-space:pre-wrap;">  </span><span style="color:#a71d5d;vertical-align:baseline;white-space:pre-wrap;">return</span><span style="vertical-align:baseline;white-space:pre-wrap;"> gulp.src(</span><span style="color:#183691;vertical-align:baseline;white-space:pre-wrap;">'./Content/**/*.less'</span><span style="vertical-align:baseline;white-space:pre-wrap;">)</span></span></p></td></tr><tr style="height:0px;"><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"> 
                        <br> 
                     </td><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"><p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
                           <span style="vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;">  .pipe(plumber())</span></p></td></tr><tr style="height:0px;"><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"> 
                        <br> 
                     </td><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"><p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
                           <span style="vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;">    .pipe(less({</span></p></td></tr><tr style="height:0px;"><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"> 
                        <br> 
                     </td><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"><p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
                           <span style="font-size:11pt;font-family:arial;">
                              <span style="vertical-align:baseline;white-space:pre-wrap;">        paths</span><span style="color:#a71d5d;vertical-align:baseline;white-space:pre-wrap;">:</span><span style="vertical-align:baseline;white-space:pre-wrap;"> [</span><span style="vertical-align:baseline;white-space:pre-wrap;"></span><span style="vertical-align:baseline;white-space:pre-wrap;">path.</span><span style="color:#0086b3;vertical-align:baseline;white-space:pre-wrap;">join</span><span style="vertical-align:baseline;white-space:pre-wrap;">(</span><span style="color:#0086b3;vertical-align:baseline;white-space:pre-wrap;">__dirname</span><span style="vertical-align:baseline;white-space:pre-wrap;">, </span> 
                              <span style="color:#183691;vertical-align:baseline;white-space:pre-wrap;">'less'</span><span style="vertical-align:baseline;white-space:pre-wrap;">, </span> 
                              <span style="color:#183691;vertical-align:baseline;white-space:pre-wrap;">'includes'</span><span style="vertical-align:baseline;white-space:pre-wrap;">)]</span></span></p></td></tr><tr style="height:0px;"><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"> 
                        <br> 
                     </td><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"><p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
                           <span style="vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;">   }))</span></p></td></tr><tr style="height:0px;"><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"> 
                        <br> 
                     </td><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"><p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
                           <span style="font-size:11pt;font-family:arial;">
                              <span style="vertical-align:baseline;white-space:pre-wrap;">    .pipe(gulp.dest(</span><span style="color:#183691;vertical-align:baseline;white-space:pre-wrap;">'./content/'</span><span style="vertical-align:baseline;white-space:pre-wrap;">));</span></span></p></td></tr><tr style="height:0px;"><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"> 
                        <br> 
                     </td><td style="border:0px solid #000000;vertical-align:top;padding:1px 11px 7px;"><p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
                           <span style="vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;"></span></p></td></tr></tbody></table></div> 
         <p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
            <span style="color:#000000;vertical-align:baseline;white-space:pre-wrap;font-size:11pt;font-family:arial;background-color:transparent;">
<a href="http://blog.chrisbriggsy.com/Gulp-101-CSS-all-the-LESS/" title="Glup 101 in Visual Studio 2015!" target="_blank">Glup 101 in Visual Studio 2015​ ​​</a>​​</span></p> 
         <p dir="ltr" style="line-height:1.38;margin-top:0pt;margin-bottom:0pt;"> 
            <br> 
         </p></span></div></span>


