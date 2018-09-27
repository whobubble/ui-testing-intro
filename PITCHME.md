# UI Testing w/ Cypress

---

- 1. What can we test?
- 2. What can't we test?
- 3. What can't we test YET?
- 4. How to write a test

---

### What can we test?

|                             | set | assert | debug |
| --------------------------- | --- | ------ | ----- |
| DOM nodes                   |     | ✓      | ✓     |
| user input / browser events | ✓   | ✓      |       |
| network traffic (HTTP)      | ✓   | ✓      | ✓     |
| call shell script           | ✓   |        |       |
| screenshots                 | ✓   | ✓      | ✓     |
| video                       | ✓   |        |       |
| navigation                  | ✓   | ✓      |       |

---

### What can't we test?

- Websocket "live updates"
  - approach:
  - 1. visit page you expect to change
  - 2. effect the change via API \*
- Dashboard (bigger org)
- headed in Cloud (regression testing)
- multiple Browsers

---

### What can't we test?

- multiple origins (e.g. app, then Gmail)
- multiple browser windows
- native events (e.g. file upload)
- multiple browser tabs

---

### How to write a test

- 1. cypress open
- 2. create or reuse spec file
- 3. minimal setup (user, data, nav path etc.)
- 4. minimal assertions a.k.a. what do i want to test
- 5. write test (save -> see test run, it.only)
