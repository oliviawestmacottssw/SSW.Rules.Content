---
type: rule
title: Do you warn users before starting a long process?
uri: do-you-warn-users-before-starting-a-long-process
created: 2018-04-25T20:50:36.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

You should never start a long process (>30 seconds) without first giving a warning message to warn the user approximately how long it will take.

[[goodExample]]
| ![Code Auditor message warning this is a long process](lengthyoperation.jpg)

You will need to have 2 things:

1. A table to record processes containing the following fields:
    - ALogRecord (DateCreated, FunctionName, EmpUpdated, ComputerName, ActiveForm, ActiveControl, SystemsResources, ConventionalMemory, FormsCount, TimeStart, TimeEnd, TimeTaken, RecordsProcessed, Avg, Note, RowGuide, SSWTimeStamp)
2. A function to change the number of seconds lapsed to words - see the "1 minute, 9 seconds" in the above messagebox - this requires a SecondsToWords() function shown. See our [code base](https://www.ssw.com.au/ssw/Standards/Rules/RulestoBetterCode.aspx#).
