# API Test Cases - DummyJSON E-Commerce API

**Base URL:** https://dummyjson.com<br>
**Tool:** Postman

| ID | Test Case | Method | Endpoint | Test Data | Expected Result | Status |
|---|---|---|---|---|---|---|
| API-TC-01 | Get all products | GET | /products | none | 200 OK, a non-empty list of products, response time under 2000 ms | Pass |
| API-TC-02 | Get a single product | GET | /products/1 | product id 1 | 200 OK, the product returned has id 1 | Pass |
| API-TC-03 | Search for products | GET | /products/search?q=phone | search word "phone" | 200 OK, a list of matching products | Pass |
| API-TC-04 | Get a product that does not exist | GET | /products/999999 | product id 999999 | 404 Not Found, an error message is returned | Pass |
| API-TC-05 | Login with valid credentials | POST | /auth/login | username "emilys", password "emilyspass" | 200 OK, an access token is returned | Pass |
| API-TC-06 | Login with a wrong password | POST | /auth/login | username "emilys", password "wrongpass" | 400 Bad Request, message "Invalid credentials" | Pass |

## Test types covered
- **Positive tests:** API-TC-01, 02, 03, 05 (valid requests that should work)
- **Negative tests:** API-TC-04, 06 (invalid requests that should be rejected correctly)

## Notes
- Each test case has automated checks written in the Postman Scripts tab (13 checks in total).
- DummyJSON is a practice API. It only pretends to save changes, so create, update and delete requests are not part of this test set.