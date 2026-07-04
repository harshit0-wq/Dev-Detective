# Dev-Detective — GitHub Profile & Repository Search Client (Sprint 03)

A responsive and asynchronous client-side application built to search GitHub profiles and repositories using the official GitHub REST API. This project was developed as part of Sprint 03 to demonstrate core JavaScript concepts including asynchronous programming, API integration, JSON parsing, DOM manipulation, Promise handling, and concurrent request execution using Vanilla JavaScript without relying on frontend frameworks.

The project intentionally uses Vanilla JavaScript to establish a strong understanding of native browser APIs, event loops, asynchronous workflows, manual state management, and dynamic DOM rendering before transitioning to declarative frameworks such as React.

## Live Deployment

**🚀 Live Demo:** [Add Deployment URL Here]


---

## Features

### Core MVP

* Real-time GitHub profile search using the GitHub REST API.
* Dynamic rendering of user information including:

  * Profile Image
  * Name
  * Username
  * Bio
  * Location
  * Join Date
* Input validation to prevent empty searches.
* Loading spinner displayed while API requests are processed.
* Custom error handling for invalid usernames and failed API requests.

### Repository Integration

* Automatic retrieval of repository information using chained API requests.
* Dynamic rendering of the latest five repositories.
* Display of repository metadata including:

  * Repository Name
  * Star Count
  * Programming Language
  * Repository Link
* Repository links open in a new browser tab.
* Human-readable formatting of GitHub timestamps and account creation dates.

### Battle Mode

* Interactive toggle allowing comparison between two GitHub users.
* Simultaneous API requests using `Promise.all()` for improved performance.
* Automatic calculation of total stars across all repositories using `.reduce()`.
* Dynamic comparison of developer profiles based on total stars.
* Conditional UI rendering including:

  * Winner highlight with green styling and badge.
  * Loser styling with reduced emphasis and grayscale effect.

## Technical Highlights

### Asynchronous JavaScript Architecture

The application uses modern `async/await` syntax to manage API requests while keeping the interface responsive and non-blocking.

### Promise Management

`Promise.all()` is used in Battle Mode to execute multiple API requests concurrently, reducing total waiting time compared to sequential execution.

### Error Handling

HTTP status codes are explicitly validated before JSON parsing.

Special handling exists for:

* `404 Not Found` for invalid usernames.
* `403 Forbidden` when GitHub API rate limits are exceeded.

### Functional Array Operations

The application utilizes native array methods including:

* `.map()`
* `.reduce()`
* `.slice()`
* `.sort()`

to efficiently process and transform repository data.

## APIs Used

### GitHub REST API

* Retrieves GitHub user profiles and repository information.
* Provides developer metadata, repositories, star counts, and account details.
* Supports real-time search functionality without requiring backend infrastructure.

### Google Fonts API

* Loads the Space Mono font to create a developer-focused interface.

### Font Awesome

* Provides icons for GitHub branding, profile information, and actions.

## Technologies Used

* HTML5
* Tailwind CSS
* Vanilla JavaScript (ES6+)
* Fetch API
* Async/Await
* Promises
* GitHub REST API
* Font Awesome
* Google Fonts

## Testing

To verify functionality:

* Search for a valid GitHub username and confirm profile details render correctly.
* Search for an invalid username and verify that the error message appears.
* Verify that the loading spinner displays during API requests.
* Confirm that exactly five repositories are displayed.
* Test repository links and verify they open in a new tab.
* Enable Battle Mode and compare two valid GitHub users.
* Verify that winner and loser visual states are applied correctly.
* Test multiple searches to ensure application state updates correctly.

**Note:** GitHub's unauthenticated API has a limit of **60 requests per hour per IP address**. If this threshold is exceeded, the API will return a `403 Forbidden` response until the limit resets.

## Conclusion

The final implementation combines API integration, asynchronous programming, concurrent request execution, dynamic DOM rendering, and resilient error handling into a single self-contained application while demonstrating strong proficiency in Vanilla JavaScript and modern frontend engineering fundamentals.
