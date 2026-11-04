# API Test Summary - DummyJSON E-Commerce API

Total test cases: 6<br>
Automated checks: 13<br>
Passed: 13<br>
Failed: 0<br>
Errors: 0<br>
Average response time: 423 ms

Failures:

* None - all checks passed.

Observations:

* All endpoints returned the expected status codes (200, 404 and 400).
* The 404 on a non-existing product is the correct, expected behaviour.
* Invalid login is rejected with a clear "Invalid credentials" message.
* Response times were low, with all requests answering in under 1 second.

Recommendations: Add create, update and delete tests when moving to REST Assured in a later project.

Tester: Asisipho Nosasa