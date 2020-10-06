---
type: rule
title: Do you use comments not exclusion files when you ignore a Code Analysis rule?
uri: do-you-use-comments-not-exclusion-files-when-you-ignore-a-code-analysis-rule
created: 2012-06-12T14:17:49.0000000Z
authors:
- id: 3
  title: Eric Phan

---

When running code analysis you may need to ignore some rules that aren't relevant to your application. Visual Studio has a handy way of doing thing. 
[[goodExample]]
| ![The Solution and Projects are named consistently](code-analysis-bad-example.jpg)
![](code-analysis-good-example.jpg)

```
public partial class Account
    {
        [System.Diagnostics.CodeAnalysis.SuppressMessage("Microsoft.Usage", "CA2214:DoNotCallOverridableMethodsInConstructors", Justification="Gold Plating")]
        public Account()
        {
            this.Centres = new HashSet();
            this.AccountUsers = new HashSet();
            this.Campaigns = new HashSet();
```

Figure: Good Example - The Solution and Projects are named consistently
