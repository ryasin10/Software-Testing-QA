# Cypress Commands

This README explains how Cypress commands work and how they are classified into four main categories:

- Queries
- Assertions
- Actions
- Other Commands

---

# Table of Contents

1. [What Are Cypress Commands?](#what-are-cypress-commands)
2. [Command Queue and Chaining](#command-queue-and-chaining)
3. [Subjects](#subjects)
4. [Retry-ability](#retry-ability)
5. [Queries](#queries)
6. [Assertions](#assertions)
7. [Actions](#actions)
8. [Other Commands](#other-commands)
9. [Complete Examples](#complete-examples)
10. [Quick Summary](#quick-summary)

---

# What Are Cypress Commands?

Cypress commands are the commands used to interact with an application and write automated tests.

For example:

```javascript
cy.visit('/login')
cy.get('#username')
cy.type('Reem')
cy.click()
cy.should('be.visible')
```

An important concept in Cypress is that commands do not execute immediately when they are invoked. Instead, Cypress queues the commands and runs them later in the correct order.

---

# Command Queue and Chaining

Consider the following example:

```javascript
cy.visit('/login')
cy.get('#username')
cy.type('Reem')
cy.click()
```

Cypress places these commands in a command queue and executes them in order:

```text
1. cy.visit('/login')
2. cy.get('#username')
3. cy.type('Reem')
4. cy.click()
```

Commands can also be chained together:

```javascript
cy.get('#username')
  .type('Reem')
  .should('have.value', 'Reem')
```

Cypress manages the command chain and the asynchronous execution for you.

---

# Subjects

A **subject** is the value or element yielded by one command and passed to the next command in a chain.

For example:

```javascript
cy.get('#username')
```

This command finds an element such as:

```html
<input id="username">
```

That element becomes the subject for the next command:

```javascript
cy.get('#username')
  .type('Reem')
```

The flow is:

```text
cy.get('#username')
        ↓
   Username Input
        ↓
      .type()
```

---

# Retry-ability

One of Cypress's important features is **retry-ability**.

Some commands automatically retry until the expected condition is met or the command times out.

For example:

```javascript
cy.get('.message')
  .should('contain', 'Success')
```

If the message does not immediately contain `Success`, Cypress can retry while waiting for the application to reach the expected state.

```text
Not Ready
   ↓
Retry
   ↓
Retry
   ↓
Success
   ↓
PASS
```

---

# Queries

## What Are Queries?

Queries are Cypress commands that read the state of your application. They return a subject for later commands to act on or assert against.

In simple terms:

```text
Query = Find / Read
```

Queries can retry as needed so that the elements or data they yield are up to date.

---

## `.as()`

Assigns an alias for later use.

```javascript
cy.get('#username')
  .as('username')

cy.get('@username')
  .type('Reem')
```

---

## `.children()`

Gets the children of each element in the current set of DOM elements.

```javascript
cy.get('.menu')
  .children()
```

Example:

```html
<div class="menu">
  <button>Home</button>
  <button>About</button>
</div>
```

---

## `.closest()`

Gets the closest ancestor that matches a selector.

```javascript
cy.get('#email')
  .closest('.form-group')
```

---

## `.contains()`

Finds a DOM element based on its text content.

```javascript
cy.contains('Login')
  .click()
```

---

## `.document()`

Gets the `window.document` object of the active page.

```javascript
cy.document()
```

---

## `.eq()`

Selects an element by its index from a collection.

```javascript
cy.get('button')
  .eq(1)
```

Indexes start at `0`.

```text
.eq(0) → First element
.eq(1) → Second element
.eq(2) → Third element
```

---

## `.filter()`

Filters elements using a selector.

```javascript
cy.get('.user')
  .filter('.active')
```

---

## `.find()`

Finds descendant elements within the previously yielded subject.

```javascript
cy.get('.form')
  .find('input')
```

The difference is:

```text
get()  → Searches from the page/document
find() → Searches inside the current subject
```

---

## `.first()`

Selects the first element in a collection.

```javascript
cy.get('.product')
  .first()
```

---

## `.focused()`

Gets the DOM element that currently has focus.

```javascript
cy.focused()
  .should('have.attr', 'id', 'username')
```

---

## `.get()`

One of the most commonly used Cypress queries. It finds DOM elements using a selector or retrieves a previously created alias.

```javascript
cy.get('#username')
```

Other examples:

```javascript
cy.get('.login-button')
```

```javascript
cy.get('[data-testid="login"]')
```

Using an alias:

```javascript
cy.get('@username')
```

---

## `.hash()`

Gets the URL hash of the active page.

If the URL is:

```text
https://example.com/products#shoes
```

You can write:

```javascript
cy.hash()
  .should('eq', '#shoes')
```

This verifies that the current URL hash is `#shoes`.

---

## `.invoke()`

Invokes a function on the previously yielded subject.

```javascript
cy.get('#username')
  .invoke('val')
```

Another example:

```javascript
cy.get('.title')
  .invoke('text')
```

---

## `.its()`

Gets the value of a property on the previously yielded subject.

```javascript
cy.location()
  .its('pathname')
```

A simple difference:

```text
its()    → Gets a property
invoke() → Calls a function
```

---

## `.last()`

Selects the last element in a collection.

```javascript
cy.get('.product')
  .last()
```

---

## `.location()`

Gets the `window.location` object of the active page.

```javascript
cy.location('pathname')
  .should('eq', '/dashboard')
```

---

## `.next()`

Gets the next sibling element.

```javascript
cy.contains('First')
  .next()
```

---

## `.nextAll()`

Gets all following sibling elements.

```javascript
cy.contains('First')
  .nextAll()
```

---

## `.nextUntil()`

Gets following sibling elements until reaching a selector.

```javascript
cy.get('.start')
  .nextUntil('.stop')
```

---

## `.not()`

Filters out elements that match a selector.

```javascript
cy.get('.user')
  .not('.active')
```

---

## `.parent()`

Gets the direct parent of a DOM element.

```javascript
cy.get('#email')
  .parent()
```

---

## `.parents()`

Gets all parent elements of a DOM element.

```javascript
cy.get('#email')
  .parents()
```

---

## `.parentsUntil()`

Gets parent elements until reaching a selector.

```javascript
cy.get('#email')
  .parentsUntil('.page')
```

---

## `.prev()`

Gets the previous sibling element.

```javascript
cy.contains('Second')
  .prev()
```

---

## `.prevAll()`

Gets all previous sibling elements.

```javascript
cy.contains('Fourth')
  .prevAll()
```

---

## `.prevUntil()`

Gets previous sibling elements until reaching a selector.

```javascript
cy.get('.current')
  .prevUntil('.stop')
```

---

## `.root()`

Gets the root DOM element.

```javascript
cy.root()
```

---

## `.shadow()`

Traverses into the Shadow DOM of an element.

```javascript
cy.get('my-component')
  .shadow()
  .find('button')
```

---

## `.siblings()`

Gets all sibling elements.

```javascript
cy.get('.current')
  .siblings()
```

---

## `.title()`

Gets the document title of the active page.

```javascript
cy.title()
  .should('eq', 'Login Page')
```

---

## `.url()`

Gets the URL of the active page.

```javascript
cy.url()
  .should('include', '/login')
```

---

## `.window()`

Gets the `window` object of the active page.

```javascript
cy.window()
```

---

# Assertions

## What Are Assertions?

Assertions are used to verify the state of an application.

In simple terms:

```text
Assertion = Verify / Check
```

Assertions automatically retry until they pass or time out.

---

## `.should()`

The main assertion command in Cypress.

```javascript
cy.get('#username')
  .should('be.visible')
```

Other examples:

```javascript
cy.get('#username')
  .should('have.value', 'Reem')
```

```javascript
cy.get('.message')
  .should('contain', 'Success')
```

```javascript
cy.get('.error')
  .should('not.exist')
```

Common assertions include:

- `be.visible`
- `exist`
- `not.exist`
- `have.value`
- `contain`
- `have.text`

---

## `.and()`

`.and()` is an alias for `.should()` and is commonly used to add another assertion to the same chain.

```javascript
cy.get('#username')
  .should('be.visible')
  .and('have.value', 'Reem')
```

This checks that the element:

1. Is visible.
2. Has the expected value.

---

# Actions

## What Are Actions?

Actions are Cypress commands that interact with the application like a user would.

```text
Action = Interact
```

Before performing an action, Cypress waits for the element to become actionable.

---

## `.check()`

Checks a checkbox or radio button.

```javascript
cy.get('#terms')
  .check()
  .should('be.checked')
```

---

## `.clear()`

Clears the value of an input or textarea.

```javascript
cy.get('#email')
  .clear()
```

---

## `.click()`

Clicks a DOM element.

```javascript
cy.get('#login')
  .click()
```

---

## `.dblclick()`

Double-clicks a DOM element.

```javascript
cy.get('.file')
  .dblclick()
```

---

## `.rightclick()`

Right-clicks a DOM element.

```javascript
cy.get('.item')
  .rightclick()
```

---

## `.scrollIntoView()`

Scrolls an element into the viewport.

```javascript
cy.get('#submit')
  .scrollIntoView()
```

---

## `.scrollTo()`

Scrolls to a specific position.

```javascript
cy.scrollTo('bottom')
```

Or:

```javascript
cy.scrollTo('top')
```

The difference is:

```text
scrollIntoView() → Scrolls to a specific element
scrollTo()       → Scrolls to a specific position
```

---

## `.select()`

Selects an option inside a `<select>` element.

```javascript
cy.get('#country')
  .select('Palestine')
```

---

## `.selectFile()`

Selects a file in an HTML file input or simulates dragging a file into the browser.

```javascript
cy.get('input[type="file"]')
  .selectFile('cypress/fixtures/photo.png')
```

---

## `.trigger()`

Triggers an event on a DOM element.

```javascript
cy.get('#help')
  .trigger('mouseover')
```

---

## `.type()`

Types text into an input or textarea.

```javascript
cy.get('#username')
  .type('Reem')
```

---

## `.uncheck()`

Unchecks a checkbox.

```javascript
cy.get('#terms')
  .uncheck()
  .should('not.be.checked')
```

---

# Other Commands

Other commands are useful commands that do not fit directly into the Query, Assertion, or Action categories.

---

## `.blur()`

Removes focus from an element.

```javascript
cy.get('#email')
  .blur()
```

---

# Cookies

## `.clearAllCookies()`

Clears all browser cookies.

```javascript
cy.clearAllCookies()
```

---

## `.clearCookies()`

Clears cookies for the current domain.

```javascript
cy.clearCookies()
```

---

## `.clearCookie()`

Clears a specific cookie.

```javascript
cy.clearCookie('session_id')
```

---

## `.getAllCookies()`

Gets all browser cookies.

```javascript
cy.getAllCookies()
```

---

## `.getCookie()`

Gets a cookie by name.

```javascript
cy.getCookie('session_id')
```

---

## `.getCookies()`

Gets cookies for the current domain.

```javascript
cy.getCookies()
```

---

## `.setCookie()`

Creates or updates a cookie.

```javascript
cy.setCookie('username', 'Reem')
```

---

# Local Storage

## `.clearAllLocalStorage()`

Clears local storage for all origins accessed during the test.

```javascript
cy.clearAllLocalStorage()
```

---

## `.clearLocalStorage()`

Clears local storage for the current domain or subdomain.

```javascript
cy.clearLocalStorage()
```

---

## `.getAllLocalStorage()`

Gets local storage data for all origins accessed during the test.

```javascript
cy.getAllLocalStorage()
```

---

# Session Storage

## `.clearAllSessionStorage()`

Clears session storage for all origins accessed during the test.

```javascript
cy.clearAllSessionStorage()
```

---

## `.getAllSessionStorage()`

Gets session storage data.

```javascript
cy.getAllSessionStorage()
```

---

## `.clock()`

Controls browser time functions such as `Date` and timers.

```javascript
cy.clock()
```

---

## `.tick()`

Moves time forward after using `cy.clock()`.

```javascript
cy.clock()
cy.tick(5000)
```

This moves time forward by 5 seconds.

---

## `.debug()`

Adds a debugger statement and helps inspect the current subject.

```javascript
cy.get('#username')
  .debug()
```

---

## `.each()`

Runs a callback for each item in an array or collection.

```javascript
cy.wrap(['Apple', 'Banana', 'Orange'])
  .each((fruit) => {
    cy.log(fruit)
  })
```

---

## `.env()`

Accesses environment variables.

```javascript
cy.env('API_URL')
```

---

## `.fixture()`

Loads fixed test data from a file.

```javascript
cy.fixture('users.json')
```

Example structure:

```text
cypress/
└── fixtures/
    └── users.json
```

---

## `.focus()`

Places focus on a DOM element.

```javascript
cy.get('#email')
  .focus()
```

---

## `.go()`

Navigates through browser history.

```javascript
cy.go('back')
```

Or:

```javascript
cy.go('forward')
```

---

## `.intercept()`

Spies on or stubs network requests and responses.

```javascript
cy.intercept('GET', '/api/users')
  .as('getUsers')

cy.visit('/users')

cy.wait('@getUsers')
```

---

## `.log()`

Prints a message in the Cypress Command Log.

```javascript
cy.log('User logged in successfully')
```

---

## `.mount()`

Used in Cypress Component Testing to mount a component.

```javascript
cy.mount(<LoginButton />)
```

---

## `.origin()`

Allows commands to run against a different origin within the same test.

```javascript
cy.origin('https://accounts.example.com', () => {
  // Cypress commands
})
```

---

## `.pause()`

Pauses test execution.

```javascript
cy.pause()
```

This is useful while debugging.

---

## `.press()`

Simulates native keyboard events.

```javascript
cy.press('TAB')
```

---

## `.prompt()`

Uses natural language to generate Cypress tests with AI-supported functionality.

---

## `.readFile()`

Reads a file from disk.

```javascript
cy.readFile('cypress/fixtures/users.json')
```

---

## `.reload()`

Reloads the current page.

```javascript
cy.reload()
```

---

## `.request()`

Makes an HTTP request directly.

```javascript
cy.request('GET', '/api/users')
```

This is useful for API testing.

---

## `.screenshot()`

Takes a screenshot of the application.

```javascript
cy.screenshot()
```

---

## `.session()`

Caches and restores browser session data, such as:

- Cookies
- localStorage
- sessionStorage

Conceptually:

```text
Login
  ↓
Create Session
  ↓
Cache Session
  ↓
Next Test
  ↓
Restore Session
```

This can avoid repeating the same login process in multiple tests.

---

## `.spy()`

Wraps a function to record its calls without replacing its original behavior.

Conceptually:

```text
Function
   ↓
Spy
   ↓
Record Calls
```

---

## `.stub()`

Replaces a method and allows you to control its behavior.

Conceptually:

```text
Original Method
      ↓
     Stub
      ↓
Controlled Behavior
```

---

## `.submit()`

Submits an HTML form.

```javascript
cy.get('form')
  .submit()
```

---

## `.task()`

Executes code in the Node environment through Cypress tasks.

Conceptually:

```text
Cypress Test
     ↓
 task()
     ↓
Node Environment
```

---

## `.then()`

Runs a callback using the current subject.

```javascript
cy.get('#username')
  .then(($username) => {
    console.log($username)
  })
```

It is useful when you need to perform JavaScript logic using a value yielded by Cypress.

---

## `.spread()`

Similar to `.then()`, but invokes a callback with multiple arguments.

---

## `.viewport()`

Controls the browser viewport size and orientation.

```javascript
cy.viewport(1280, 720)
```

Example for responsive testing:

```javascript
cy.viewport('iphone-6')
```

---

## `.visit()`

Visits a URL.

```javascript
cy.visit('/login')
```

Many Cypress tests begin with `cy.visit()`.

---

## `.wait()`

Can wait for a specific amount of time:

```javascript
cy.wait(2000)
```

It can also wait for an aliased request:

```javascript
cy.intercept('GET', '/api/users')
  .as('getUsers')

cy.wait('@getUsers')
```

Waiting for a specific request is generally more meaningful than using an unnecessary fixed delay.

---

## `.within()`

Scopes subsequent commands to a specific element.

```javascript
cy.get('#login').within(() => {
  cy.get('[name="email"]')
    .type('test@example.com')

  cy.get('[name="password"]')
    .type('123456')
})
```

This is useful when similar elements exist in multiple parts of a page.

---

## `.wrap()`

Wraps an object or value so it can be used inside a Cypress command chain.

```javascript
const user = {
  name: 'Reem'
}

cy.wrap(user)
```

---

## `.writeFile()`

Writes content to a file.

```javascript
cy.writeFile('result.txt', 'Test completed')
```

---

# Deprecated Commands

Some commands may be marked as **deprecated** in Cypress documentation. Deprecated commands should generally not be the focus when learning modern Cypress.

---

# Complete Examples

## Example 1: Login Test

```javascript
cy.visit('/login') // Other

cy.get('#email') // Query
  .type('test@example.com') // Action

cy.get('#password') // Query
  .type('123456') // Action

cy.get('#remember') // Query
  .check() // Action

cy.get('#login') // Query
  .click() // Action

cy.get('.dashboard') // Query
  .should('be.visible') // Assertion
```

---

## Example 2: Query → Action → Assertion

```javascript
cy.get('#username')
  .type('Reem')
  .should('have.value', 'Reem')
```

Classification:

```text
cy.get()    → Query
.type()     → Action
.should()   → Assertion
```

---

## Example 3: URL Navigation

```javascript
cy.get('#login')
  .click()

cy.location('pathname')
  .should('eq', '/dashboard')
```

---

## Example 4: URL Hash

If the URL becomes:

```text
https://example.com/products#shoes
```

You can verify the hash with:

```javascript
cy.hash()
  .should('eq', '#shoes')
```

---

## Example 5: Network Request

```javascript
cy.intercept('GET', '/api/users')
  .as('getUsers')

cy.visit('/users')

cy.wait('@getUsers')
```

---

# Quick Summary

## Queries

Used to find or read application state.

```text
Query = Find / Read
```

Examples:

```javascript
cy.get()
cy.contains()
cy.find()
cy.first()
cy.last()
cy.eq()
cy.url()
cy.title()
cy.location()
```

---

## Assertions

Used to verify application state.

```text
Assertion = Verify / Check
```

Commands:

```javascript
.should()
.and()
```

---

## Actions

Used to interact with the application.

```text
Action = Interact
```

Examples:

```javascript
.click()
.type()
.check()
.uncheck()
.clear()
.select()
```

---

## Other Commands

Useful commands for setting up, controlling, debugging, and managing tests.

Examples:

```javascript
cy.visit()
cy.intercept()
cy.request()
cy.fixture()
cy.session()
cy.wait()
cy.then()
cy.within()
cy.wrap()
```

---

# The Main Cypress Flow

A common Cypress testing pattern is:

```text
OTHER
  ↓
QUERY
  ↓
ACTION
  ↓
QUERY
  ↓
ASSERTION
```

In simple terms:

> **Open → Find → Interact → Find → Verify**

Example:

```javascript
cy.visit('/login')

cy.get('#email')
  .type('test@example.com')

cy.get('#login')
  .click()

cy.get('.dashboard')
  .should('be.visible')
```

---

# Final Summary

```text
Query
  ↓
Find / Read
  ↓
Subject
  ↓
Action
  ↓
Interact
  ↓
Application Changes
  ↓
Assertion
  ↓
Verify
  ↓
PASS / FAIL
```

The easiest way to remember the command categories is:

> **Query = Find**  
> **Action = Do**  
> **Assertion = Check**  
> **Other = Test Helpers**
