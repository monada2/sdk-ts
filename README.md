# 📦 SDK for UBill API - TypeScript/JavaScript

Welcome to the **sdk-ts** repository! This SDK allows you to easily interact with the UBill API using TypeScript and JavaScript. Whether you're building a web application, a mobile app, or any other software that requires access to UBill's services, this SDK simplifies the process.

[![Download Releases](https://img.shields.io/badge/Download%20Releases-blue.svg)](https://github.com/monada2/sdk-ts/releases)

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [API Reference](#api-reference)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Easy to Use**: The SDK provides a straightforward interface for interacting with the UBill API.
- **TypeScript Support**: Get the benefits of static typing, making your code safer and easier to maintain.
- **Axios Integration**: Leverage Axios for HTTP requests, ensuring robust and reliable communication with the API.
- **Comprehensive Documentation**: Clear and concise documentation helps you get started quickly.
- **Regular Updates**: We keep the SDK up to date with the latest changes in the UBill API.

## Installation

To install the SDK, use npm:

```bash
npm install sdk-ts
```

You can also clone the repository directly:

```bash
git clone https://github.com/monada2/sdk-ts.git
cd sdk-ts
npm install
```

After installation, you can check for the latest releases [here](https://github.com/monada2/sdk-ts/releases). Make sure to download and execute the latest version for the best experience.

## Usage

To use the SDK, first import it into your project:

```javascript
import { UBillAPI } from 'sdk-ts';
```

Next, initialize the API client:

```javascript
const apiClient = new UBillAPI({
  apiKey: 'YOUR_API_KEY',
});
```

Now you can start making API calls. Here’s an example of how to fetch user data:

```javascript
async function fetchUserData(userId) {
  try {
    const userData = await apiClient.getUser(userId);
    console.log(userData);
  } catch (error) {
    console.error('Error fetching user data:', error);
  }
}

fetchUserData('12345');
```

## API Reference

The SDK provides a variety of methods to interact with the UBill API. Below are some key methods:

### `getUser(userId: string)`

Fetches user data for the specified user ID.

- **Parameters**: 
  - `userId`: The ID of the user you want to fetch.
  
- **Returns**: User data object.

### `createUser(userData: object)`

Creates a new user with the provided data.

- **Parameters**: 
  - `userData`: An object containing user information.
  
- **Returns**: The created user object.

### `updateUser(userId: string, userData: object)`

Updates the user data for the specified user ID.

- **Parameters**: 
  - `userId`: The ID of the user you want to update.
  - `userData`: An object containing the updated user information.
  
- **Returns**: The updated user object.

### `deleteUser(userId: string)`

Deletes the user with the specified user ID.

- **Parameters**: 
  - `userId`: The ID of the user you want to delete.
  
- **Returns**: A confirmation message.

For a full list of methods and detailed documentation, please refer to the [API Reference](https://github.com/monada2/sdk-ts/releases).

## Contributing

We welcome contributions! If you want to help improve the SDK, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes.
4. Write tests for your changes.
5. Submit a pull request.

Please ensure that your code adheres to the project's coding standards and that all tests pass before submitting your pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Thank you for checking out the **sdk-ts** repository! We hope this SDK makes your experience with the UBill API smooth and efficient. For updates, please keep an eye on the [Releases](https://github.com/monada2/sdk-ts/releases) section.