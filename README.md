
# API Testing - DummyJSON E-Commerce API

## Project Overview
This project tests a practice e-commerce REST API using Postman. It checks products, search and login, including requests that are supposed to fail, and uses automated checks to confirm each result.

**API under test:** [DummyJSON](https://dummyjson.com/)

## Tools Used
- Postman (requests, test scripts and Collection Runner)
- GitHub (version control)

## What Was Tested
| ID | Test Case | Method | Endpoint | Expected |
|---|---|---|---|---|
| API-TC-01 | Get all products | GET | /products | 200 OK |
| API-TC-02 | Get a single product | GET | /products/1 | 200 OK |
| API-TC-03 | Search for products | GET | /products/search?q=phone | 200 OK |
| API-TC-04 | Get a non-existing product | GET | /products/999999 | 404 Not Found |
| API-TC-05 | Login with valid credentials | POST | /auth/login | 200 OK + token |
| API-TC-06 | Login with a wrong password | POST | /auth/login | 400 Bad Request |

## Results
**13 of 13 automated checks passed.** Average response time was 423 ms.

## Project Structure
- [docs](./docs) - [API test cases](./docs/API_Test_Cases.md)
- [postman-collection](./postman-collection) - the exported Postman collection
- [test-reports](./test-reports) - [API test summary](./test-reports/API_Test_Summary.md)
- [evidence/screenshots](./evidence/screenshots) - Postman and collection run screenshots

## How to Run the Tests
1. Open Postman and click **Import**.
2. Choose the collection file from the `postman-collection` folder.
3. Right-click the collection, choose **Run collection**, and click **Run**.

## Notes
DummyJSON is a practice API that only pretends to save changes, so create, update and delete requests are not included.

## Future Improvements
- Add REST Assured tests in Java
- Run the collection automatically with GitHub Actions
