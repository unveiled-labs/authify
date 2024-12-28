# Authify

A seamless and customizable authentication package offering pre-built sign-in and sign-up pages with complete authentication functionality. Authify is designed for developers to easily integrate user authentication, token management, and route protection into their projects. Ideal for building secure and user-friendly applications with minimal effort.

---

## Features

-   **Pre-built Sign-in and Sign-up Pages**: Easily integrate ready-to-use authentication pages.
-   **Token-Based Authentication**: Secure user authentication with JWT.
-   **Route Protection**: Simple middleware to protect routes based on user authentication.
-   **Customizable UI**: Easily style the authentication pages according to your needs.
-   **Third-party OAuth Integration**: Support for Google and GitHub authentication.

---

## Installation

To install `authify`, simply use npm:

```bash
npm install @unveiled-labs/authify
```

---

## Usage

### 1. **Integrating Authentication Pages**

Import and use the pre-built components for sign-in and sign-up:

```javascript
import { SignInPage, SignUpPage } from "@unveiled-labs/authify";

// Use SignInPage and SignUpPage wherever needed in your app
```

### 2. **Handling Authentication**

Use the provided functions for signing in and signing up users:

```javascript
import { signIn, signUp } from "@unveiled-labs/authify";

// Sign in a user
const user = signIn({ email: "user@example.com", password: "password123" });

// Sign up a new user
const newUser = signUp({
    name: "John Doe",
    email: "john@example.com",
    password: "password123",
});
```

### 3. **Protecting Routes**

Protect routes in your application by using middleware:

```javascript
import { protectRoute } from "@unveiled-labs/authify";

// Use protectRoute in your API routes to ensure only authenticated users can access them
app.get("/protected", protectRoute, (req, res) => {
    res.send("This is a protected route!");
});
```

---

## Configuration

`authify` is highly customizable to fit your application’s needs. You can style the pages and adjust configurations for JWT authentication, token expiration, and more.

---

## Running Tests

To test the package locally:

```bash
npm test
```

Make sure you have set up your `test.js` file to test authentication functionalities.

---

## Contributing

We welcome contributions! Please fork the repository, create a feature branch, and submit a pull request.

---

## Bugs and Issues

If you find a bug or have a feature request, please open an issue on the [GitHub Issues page](https://github.com/unveiled-labs/authify/issues).

---

## License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

---

This README provides basic instructions, usage examples, and contribution guidelines. You can customize it further to match any specific needs or features in your package.

Let me know if you need more modifications!
