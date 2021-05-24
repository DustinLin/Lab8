# Lab8_Starter

## Group
Dustin Lin 

## Check your understanding q's (FILL OUT)
1. In your own words: Where would you fit your automated tests in your Bujo project development pipeline? (just write the letter)
- 1

2. Would you use a unit test to test the “message” feature of a messaging application? Why or why not? For this question, assume the “message” feature allows a user to write and send a message to another user.
- We should not use a unit test here since there are actually many opertaions that go into "writing and sending a message to another user". We can break this task down further into operation like correctly capturing what the user wrote, and actually sending the message to another user.

3. Would you use a unit test to test the “max message length” feature of a messaging application? Why or why not? For this question, assume the “max message length” feature prevents the user from typing more than 80 characters
- We should use a unit test here to test the "max message length" feature. Since this is a single opertion that can't be broken down further.

4. What do you expect to happen if we run our puppeteer tests with the field “headless” set to true?
- The test would run without showing me the browser UI.

5. What would your beforeAll callback look like if you wanted to start from the settings page before every test case?
```
  beforeAll(async () => {
    await page.goto('http://127.0.0.1:5501');
    await page.waitForTimeout(500);
    await expect(page).toClick('header > img');
  });

```

