---
type: rule
title: Do you define your response types?
uri: do-you-define-your-response-types
created: 2019-05-25T02:12:33.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

It is important to define your response types.
[[badExample]]
| ![ Bad example – no response types![good-response-types.png](good-response-types.png)](bad-no-response-types.jpg)<br>dd>


/// 
/// Returns the nth number in the fibonacci sequence.
/// 
/// The index (n) of the fibonacci sequence
/// Returns the nth fibonacci number.
/// int64
[HttpGet]
[ProducesResponseType(200)]
[ProducesResponseType(400)]
[ResponseCache(CacheProfileName = DefaultCacheProfile.Name)]
[Produces("application/json", "text/json")]
public ActionResult Get(long n)
{
\_logger.LogInformation($"Fibonacci number {n} requested");
if(!\_fibonacciSolver.CanSolve(n))
return new BadRequestResult();
try
{
return \_cache.GetOrAdd($"Fibonacci{n}", () => \_fibonacciSolver.Solve(n));
}
catch (ArgumentOutOfRangeException)
{
return new BadRequestResult();
}
}
Figure: Good example for swashbuckle - Even better if you have .NET Core 2.1 use the strong typed ActionResult – see yellow


[HttpGet]
        [SwaggerResponse(HttpStatusCode.OK, typeof(long))]
        [SwaggerResponse(HttpStatusCode.BadRequest, typeof(void))]
        public ActionResult Get(long n)
        {
            \_logger.LogInformation($"Fibonacci number {n} requested");

            if(!\_fibonacciSolver.CanSolve(n))
                return new BadRequestResult();
 
            try
            {
                return \_cache.GetOrAdd($"Fibonacci{n}", () => \_fibonacciSolver.Solve(n));
            }
            catch (ArgumentOutOfRangeException)
            {
                return new BadRequestResult();
            }
        }
Figure: Good example for nswag - Even better if you have .NET Core 2.1 use the strong typed ActionResult – see yellow
