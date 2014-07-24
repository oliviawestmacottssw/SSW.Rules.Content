---
type: rule
title: Estimating - Do you know how to size user stories effectively?
uri: estimating---do-you-know-how-to-size-user-stories-effectively
created: 2010-09-01T01:15:18.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 23
  title: Damian Brady
- id: 24
  title: Adam Stephensen
- id: 45
  title: Chris Briggs

---

 
A team knows how many stories they can commit to my measuring their velocity.  The Team estimates the highest priority stories in the Product Backlog in Story Points. ​It is very important for teams to estimate tasks effectively.  There are several methods for estimating:

- Shirt Sizes
- Fibonacci Extended (1-100)
- Fibonacci Original (1-21)
- Doubling
- Thr​own


Let's go through them:​

### Shirt Sizes

This method is popular with Microsoft teams, but it has the problem of not easily mapping to the common 7 numbers when you enter it into a Task tracking Bug database. eg.


> 1 = XS
> 2 = S
> 3 = M
> 5 = L
> 8 = XL
> 13 = ?
> 21 = XXL

![](/Management/RulesToBetterScrumUsingTFS/PublishingImages/size-stories-bad-example.jpg)Figure: Bad example - Estimation using T-Shirt sizes
### Fibonacci Extended (1-100)

Planning Poker is a very effective Product Backlog estimation technique and the most common method is using Fibonacci numbers (1,2,3,5,8,13, etc.). This was made popular by Mike Cohn.
![](/Management/RulesToBetterScrumUsingTFS/PublishingImages/size-stories-ok-example.jpg)Figure: OK example - Estimation using Planning Poker with large numbers
### Fibonacci (1-21)

Mike Cohn introduced changes to the original 7 cards, by changing the 21 to 20 and adding 40 and 100 to indicate very large user stories called Epics.

Ken Schwaber (the father of Scrum) says in his Scrum Certification course, that he is not a fan of the extra cards and says he prefers teams keep to the original 7 cards.
![](/Management/RulesToBetterScrumUsingTFS/PublishingImages/size-stories-good-example.jpg)​Figure: OK example - Estimation using Planning Poker with only small numbers
### Doubling 

Estimating using doubling numbers makes relative sizing simple. An 8 point PBI should be about twice the size as a 4-point PBI. This method also simplifies PBI swapping where a PBI is replaced with PBIs totalling the same number of points.

It has one other advantage over the Fibonacci sequence, it is easier for non-techies because the numbers aren't whacky and the name isn't bizarre.


| **Estimate ** |  |
| --- | --- |
| 1 |  |
| 2 |  |
| 4 |  |
| 8 |  |
| 16 |  |
| 32 |  |
| 64 |  |

Figure: Good example -Doubling simplifies relative sizing
### Thown 

Another method of estimating is the "Thrown method" as described Martin Fowler.     [http://martinfowler.com/bliki/ThrownEstimate.html](http&#58;//martinfowler.com/bliki/ThrownEstimate.html)![](/_LAYOUTS/15/Images/SSW/external.gif "You are now leaving SSW")![](/_LAYOUTS/15/Images/SSW/external.gif "You are now leaving SSW")

This is particularly useful if you don't have Planning Poker cards.  Instead of Fibonacci numbers, estimates are from 1 to 5.  It's nice and simple, and you only need the fingers on your hand.

The action is done in the same method as the game 'Rock, Paper, Scissors'. The options the developer can estimate is 1,2,3,4,5
![](/Management/RulesToBetterScrumUsingTFS/PublishingImages/fist-method.jpg)Figure: User Story estimates using the "Thown method"
### Other Tips:

**#1 Don't Shout Out**
 It will just influence other peoples votes.

**#2 Guidelines for Estimating User Stories (aka Anchoring)**
 Every team is different, but you can use the following guidelines for sizing User Stories.


> | **Estimate Value** | **Example User Story** |
> | --- | --- |
> | 1 | A change to a messagebox |
> | 2 | - |
> | 3 | A timeboxed task for 1 day x 1 guy |
> | 5 | A timeboxed task of 1 day x 2 guys |
> | 8 | - |
> | 13 | - |
> | 21 | More than a month with a couple of guys.<br>TIP: Don't include these in a sprint because they are too risky - ask for them to be broken down. |
> 
> Figure: Good example - Example User Story estimates


**#3 Using a Chat Program**
 If you are working on a project with a remote team, use Skype chat to size stories using Planning Poker.  Everyone should give their points for stories at the same time to avoid influencing each other.

**#4 Big Stories Smell**
 PBIs of greater than 1 day are a smell and PBIs greater than 2 days are a stench. If User Stories are estimated at more than 1 or 2 days of work, consider splitting them into smaller pieces to keep them under 1 or 2 days.  See Do You Break Large Tasks into Smaller Tasks?

**#5 Use Spikes**
 If you do find a very large User Story, consider using a Spike (aka. an investigation task) to help work out how much work will be involved.

**#6 Small stories**

As some stories can be obviously very small, we allow any member of the Team to propose that a Story is 0.5 points and no further discussion is required.  If there is no objection (i.e. immediate consensus is reached) then the story is given 0.5 points and the Team move on to the next one.  This is the only way a story can have only 0.5 points and always indicates that is was a quick decision and therefore may have some risk attached.


 ​​Related rule
- [Do you estimate “Business Value”?​](/Management/RulesToBetterScrumUsingTFS/Pages/Estimate-Business-Value.aspx)


