---
type: rule
archivedreason: 
title: Do you always avoid On Error Resume Next? (VB Only)
guid: 44ff5d65-56bc-4b02-957d-378c8c0bfc5c
uri: do-you-always-avoid-on-error-resume-next-vb-only
created: 2013-09-11T22:01:01.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


<p>​​Never use On Error Resume Next in VB (and VB.NET) projects.<br>
<br>
If an error occurred, On Error Resume Next will hide the error and things can go very haywire! In .NET, stop using the On Error syntax and use the try-catch exception syntax for better structural exception handling.</p>
<br><excerpt class='endintro'></excerpt><br>
<p class="p1">In VB/VBA you should use On Error Resume Next with line of comment and after an offending line of code there should be statement On Error GoTo 0 to reset Errors collection.</p><dl class="bad"><dt><pre>Private Sub cmdSelect_Click()
    Dim varTemp As Variant
    On Error Resume Next
    varTemp = columnADOX.Properties(&quot;RelatedColumn&quot;).Value
        .
        ....many lines of code...
        .
    intRoutesPerDay = 2
    End Sub
</pre></dt><dd>Bad Example – Bad code</dd></dl><dl class="good"><dt><pre>Private Sub cmdSelect_Click()
    Dim varTemp As Variant
    On Error Resume Next
    'Sometimes there is no related column value
    varTemp = columnADOX.Properties(&quot;RelatedColumn&quot;).Value
    On Error GoTo 0

    .
    ....continuing code...
    .
    End Sub
</pre></dt><dd>Good Example – Good code</dd></dl><p class="p5"> 
   <span class="ssw-rteStyle-YellowBorderBox">We have a program called&#160;<a href="http&#58;//www.ssw.com.au/ssw/CodeAuditor/Default.aspx">SSW Code Auditor</a>&#160;to check for this rule.</span></p>


