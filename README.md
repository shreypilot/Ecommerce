# Ecommerce Website using React, Redux, Tailwind, Stripe Payment Gateway, and Firebase

This is a sample ecommerce website built using React, Redux, Tailwind, Stripe Payment Gateway, and Firebase. This project is meant to be used as a starting point for building your own ecommerce website.

## Getting Started

1. Clone the repository:

```
git clone https://github.com/your-username/ecommerce-website.git
```

2. Install the dependencies:

```
cd ecommerce-website
npm install
```

3. Set up Firebase:

   - Create a new Firebase project in the [Firebase Console](https://console.firebase.google.com/)
   - Add a new web app to the project
   - Copy the Firebase config object into a new file named `firebase.js` in the `src` directory

   ```javascript
   // src/firebase.js

   import firebase from 'firebase/app';
   import 'firebase/auth';
   import 'firebase/firestore';

   const config = {
     apiKey: 'YOUR_API_KEY',
     authDomain: 'YOUR_AUTH_DOMAIN',
     projectId: 'YOUR_PROJECT_ID',
     storageBucket: 'YOUR_STORAGE_BUCKET',
     messagingSenderId: 'YOUR_MESSAGING_SENDER_ID',
     appId: 'YOUR_APP_ID',
   };

   firebase.initializeApp(config);

   export const auth = firebase.auth();
   export const firestore = firebase.firestore();
   export const firebaseTimestamp = firebase.firestore.FieldValue.serverTimestamp();
   ```

4. Set up Stripe:

   - Create a [Stripe account](https://stripe.com/) if you don't have one already
   - Obtain your Stripe API keys from the [Stripe Dashboard](https://dashboard.stripe.com/test/apikeys)
   - Add your Stripe API keys to your `.env` file:

   ```
   REACT_APP_STRIPE_PUBLISHABLE_KEY=<your_publishable_key>
   REACT_APP_STRIPE_SECRET_KEY=<your_secret_key>
   ```

5. Run the development server:

```
npm start
```

6. Open the app in your browser:

```
http://localhost:3000
```

## Project Structure

```
├── public
│   ├── index.html
│   ├── manifest.json
│   └── robots.txt
├── src
│   ├── components
│   │   ├── AuthForm
│   │   ├── Cart
│   │   ├── CheckoutForm
│   │   ├── Collection
│   │   ├── Header
│   │   ├── Product
│   │   ├── ProductForm
│   │   ├── ProductsList
│   │   └── Spinner
│   ├── pages
│   │   ├── AuthPage
│   │   ├── CartPage
│   │   ├── CheckoutPage
│   │   ├── CollectionPage
│   │   ├── HomePage
│   │   ├── NotFoundPage
│   │   └── ProductPage
│   ├── redux
│   │   ├── cart
│   │   ├── products
│   │   ├── root-reducer.js
│   │   └── store.js
│   ├── App.js
│   ├── firebase.js
│   ├── index.js
│   ├── reportWebVitals.js
│   └── setupTests.js
├── .env
├── .gitignore
├── package-lock.json
├── package.json
└── README.md
```

## Technologies Used

- React: A JavaScript library for building user interfaces
- Redux: A predictable state container for JavaScript apps
- Tailwind CSS: A utility-first CSS framework for rapid UI development
- Stripe: A payment gateway for online businesses
- Firebase: Firebase is a backend-as-a-service platform that provides a variety of tools and services for building and managing web and mobile applications. In this project, we're using Firebase to handle user authentication and store product data in a database.

Some of the Firebase services we're using include:

- Authentication: Firebase Authentication provides a simple way to authenticate users with email and password or using other popular authentication providers like Google, Facebook, or Twitter.
- Cloud Firestore: Cloud Firestore is a flexible, scalable, and real-time NoSQL document database that stores data in documents organized into collections. We're using Firestore to store product data and manage orders.
- Firebase Hosting: Firebase Hosting provides fast and secure hosting for your web app. We're using Firebase Hosting to deploy our ecommerce website.

## Features

This ecommerce website includes the following features:

- Browse products by category or search by keyword
- View product details, including name, price, description, and images
- Add products to cart and update the quantity
- Checkout using Stripe payment gateway
- View order history and order details
- Authentication with email and password

## Contributing

If you want to contribute to this project, please feel free to submit a pull request. Before submitting a pull request, please make sure your changes are consistent with the project's style and conventions.


