---
type: rule
title: Do you look for opportunities to use Linq?
uri: do-you-look-for-opportunities-to-use-linq
created: 2012-04-01T09:23:06.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 23
  title: Damian Brady

---

Linq is a fantastic addition to .Net which lets you write clear and beautiful declarative code. Linq allows you to focus more on the  **what**  and less on the  **how** .

You should look for opportunities to replace your existing code with Linq.
 
For example, replace your foreach loops with Linq.


```
var lucrativeCustomers = new List<Customer>();
foreach (var customer in Customers)
{
    if (customer.Orders.Count > 0)
    {
        lucrativeCustomers.Add(customer);
    }
}
```

Figure: Bad Example - imperative programming using a foreach loop

```
var lucrativeCustomers = Customers.Where(c => c.Orders.Count > 0).ToList();
```

Figure: Good Example - declarative programming using Linq
