# BC01 - Authentication & Account

| TC ID | Business Context | Scenario | API | Method | Test Data | Expected Result | Status |
|---|---|---|---|---|---|---|---|
| TC01-01 | Authentication | Register with valid data | /auth/register | POST | Valid name/email/password | Account created successfully | NOT RUN |
| TC01-02 | Authentication | Register with existing email | /auth/register | POST | Existing email | Request rejected | NOT RUN |
| TC01-03 | Authentication | Register with missing required field | /auth/register | POST | Missing email/password | Validation error | NOT RUN |
| TC01-04 | Authentication | Login with valid credentials | /auth/login | POST | Valid email/password | Login successful and token returned | NOT RUN |
| TC01-05 | Authentication | Login with wrong password | /auth/login | POST | Wrong password | Authentication failed | NOT RUN |
| TC01-06 | Authentication | Login with unknown account | /auth/login | POST | Unknown email | Authentication failed | NOT RUN |
| TC01-07 | Authentication | Access protected API without token | Protected API | GET/POST | No JWT | 401 Unauthorized | NOT RUN |
| TC01-08 | Authentication | Access API with expired token | Protected API | GET/POST | Expired JWT | 401 Unauthorized | NOT RUN |
| TC01-09 | Authentication | Unverified customer creates trip | Trip API | POST | Unverified account | Request rejected | NOT RUN |
