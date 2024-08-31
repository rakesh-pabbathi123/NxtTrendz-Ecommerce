# **Nxt Trendz - Cart Features**

To build the **Nxt Trendz - Cart Features** in your e-commerce React application, follow the structured steps below. These instructions will guide you through implementing cart management, authentication, and more, while also covering key React concepts.
## Published Link
- **Build by Rakesh Pabbathi**:https://rakhinxtrendz.ccbp.tech
## Table of Contents
1. [Project Overview](#project-overview)
2. [Components Overview](#components-overview)
3. [Features to Implement](#features-to-implement)
4. [Setting Up the Project](#setting-up-the-project)
5. [Component Implementation](#component-implementation)
   - [CartContext](#cartcontext)
   - [Cart](#cart)
   - [CartItem](#cartitem)
   - [CartSummary](#cartsummary)
   - [ProtectedRoute](#protectedroute)
   - [LoginForm](#loginform)
   - [AllProductsSection](#allproductssection)
   - [CartListView](#cartlistview)
   - [EmptyCartView](#emptycartview)
   - [FiltersGroup](#filtersgroup)
   - [Header](#header)
   - [Home](#home)
   - [NotFound](#notfound)
   - [PrimeDealsSection](#primedealssection)
   - [ProductCard](#productcard)
   - [ProductItemDetails](#productitemdetails)
   - [Products](#products)
   - [ProductsHeader](#productsheader)
   - [SimilarProductItem](#similarproductitem)
6. [API Endpoints](#api-endpoints)
7. [Styling](#styling)
8. [Resources](#resources)
9. [Important Notes](#important-notes)

## Project Overview

This project is an e-commerce web application built with React, focusing on implementing robust cart features and user authentication. You'll work with various React components, manage state using context, and ensure a seamless user experience.

### Key Objectives:

- Implement cart management features such as adding, removing, and updating cart items.
- Handle authentication and protected routes.
- Display a summary of cart items and total cost.


## Features to Implement



1. **Product Listing**
   - Display a grid or list of all available products.
   - Include essential product details such as name, price, image, and rating.
   - Fetch product data from the server and handle loading states.

2. **Sorting and Filtering**
   - Implement sorting options for products by price, popularity, and rating.
   - Provide filtering options by category, price range, rating, and search terms.
   - Update the product list based on selected sorting and filtering criteria.

3. **Cart Management**
   - **Add to Cart**: Allow users to add products to their cart from the product listing or product details page.
   - **View Cart**: Display cart items with details such as product name, image, price, and quantity.
   - **Update Cart**: Allow users to update the quantity of items or remove items from the cart.
   - **Cart Summary**: Show the total price and number of items in the cart.
   - **Empty Cart Handling**: Display a message or image when the cart is empty.

4. **User Authentication**
   - **Login**: Implement user login functionality with email and password authentication.
   - **Logout**: Allow users to log out and clear their session.
   - **Protected Routes**: Restrict access to certain routes (e.g., Cart, Account) to authenticated users only.
   - **Session Management**: Store and manage user authentication tokens.

5. **Product Details**
   - **Product Information**: Display detailed information for a specific product including description, price, reviews, and related products.
   - **Add to Cart**: Allow users to add the product to their cart from the details page.

6. **Special Deals and Promotions**
   - **Prime Deals Section**: Showcase special deals, discounts, and promotions on the homepage.
   - **Highlight Deals**: Feature discounted or special offer products prominently.

7. **Filters and Search**
   - **Filters Group**: Allow users to filter products by various criteria such as categories, price range, and ratings.
   - **Search Functionality**: Implement a search bar to allow users to find products by name or keyword.

8. **User Feedback**
   - **Rating and Reviews**: Allow users to rate and review products.
   - **Product Recommendations**: Show similar products based on the currently viewed product.

9. **404 Error Page**
   - Display a friendly message or image for non-existent routes.
   - Provide a link to navigate back to the home page or another valid route.

10. **Responsive Design**
    - Ensure the application is fully responsive and functions well on various devices, including desktops, tablets, and mobile phones.

11. **Styling and Theming**
    - Implement consistent styling across the application using CSS modules or a preprocessor.
    - Provide a user-friendly and visually appealing interface.

12. **API Integration**
    - **Endpoints**: Connect to backend APIs for fetching products, managing the cart, and handling user authentication.
    - **Error Handling**: Implement error handling for failed API requests and display appropriate messages to users.

13. **State Management**
    - Use context or state management libraries to handle global state for cart, user authentication, and product data.

14. **Accessibility**
    - Ensure the application is accessible to users with disabilities by following best practices for web accessibility.

15. **Performance Optimization**
    - Optimize application performance by lazy loading components, minimizing bundle size, and improving data fetching strategies.

16. **Unit and Integration Testing**
    - Write tests for critical components and functionality to ensure the application works as expected.


## Setting Up the Project

### Prerequisites:

- Ensure you have Node.js installed.
- Install project dependencies by running:

  ```bash
  npm install
  ```

- Start the application using:

  ```bash
  npm start
  ```

## Component Implementation


### 1. **AllProductsSection**
   - **Purpose**: Displays all the products available for purchase. It handles fetching data from the API and provides sorting and filtering options to help users find products based on their preferences.
   - **Key Features**:
     - Fetch products from the server.
     - Display products in a grid or list.
     - Implement filtering by category, rating, and price.
     - Handle sorting by price, popularity, etc.

### 2. **Cart**
   - **Purpose**: Manages the user's cart. Displays the products added to the cart and allows users to update quantities or remove items.
   - **Key Features**:
     - Display cart items with the ability to update or remove them.
     - Show a summary of the cart, including the total price and number of items.
     - Integrate with `CartListView`, `CartItem`, and `CartSummary` components.

### 3. **CartItem**
   - **Purpose**: Represents a single item in the cart. It shows the product's name, image, price, and quantity.
   - **Key Features**:
     - Provide options to increase or decrease the quantity of the item.
     - Allow users to remove the item from the cart.

### 4. **CartListView**
   - **Purpose**: Displays the list of cart items in a structured format.
   - **Key Features**:
     - Iterate through cart items and display each using the `CartItem` component.
     - Handle the layout and design of the cart list.

### 5. **CartSummary**
   - **Purpose**: Shows a summary of the cart, including the total price and the number of items in the cart.
   - **Key Features**:
     - Calculate and display the total cost of all items.
     - Show the number of items in the cart.

### 6. **EmptyCartView**
   - **Purpose**: Displays a message and possibly an image when the cart is empty.
   - **Key Features**:
     - Provide a user-friendly message indicating that the cart is empty.
     - Include a call-to-action (like a button to continue shopping).

### 7. **FiltersGroup**
   - **Purpose**: Allows users to filter products based on various criteria like categories, ratings, and search terms.
   - **Key Features**:
     - Provide filtering options like category selection, price range, and rating.
     - Integrate search functionality to filter products by name or keyword.

### 8. **Header**
   - **Purpose**: Displays the application's header, which typically includes navigation links and the cart icon.
   - **Key Features**:
     - Show navigation links to different sections of the application (e.g., Home, Products, Cart).
     - Display the number of items in the cart.

### 9. **Home**
   - **Purpose**: The main landing page that users see when they first visit the application.
   - **Key Features**:
     - Display the `PrimeDealsSection`.
     - Include links to various product categories.
     - Provide a welcoming interface with featured products or deals.

### 10. **LoginForm**
   - **Purpose**: Handles user authentication by allowing users to log in.
   - **Key Features**:
     - Collect user credentials (email and password).
     - Authenticate users by sending the credentials to the server.
     - Store the authentication token in cookies for session management.

### 11. **NotFound**
   - **Purpose**: A 404 error page displayed when a user navigates to a non-existent route.
   - **Key Features**:
     - Display a friendly message or image indicating that the page is not found.
     - Provide a link to navigate back to the home page or another valid route.

### 12. **PrimeDealsSection**
   - **Purpose**: Displays a special section of the homepage dedicated to deals and promotions.
   - **Key Features**:
     - Show featured products or deals.
     - Attract users to special offers or discounted products.

### 13. **ProductCard**
   - **Purpose**: Displays individual product information such as the title, brand, price, image, and rating in a card format.
   - **Key Features**:
     - Provide a quick view of the product’s essential details.
     - Integrate with `Products` and `AllProductsSection` components.

### 14. **ProductItemDetails**
   - **Purpose**: Displays detailed information about a specific product.
   - **Key Features**:
     - Show the product’s full details, including description, price, reviews, and similar products.
     - Allow users to add the product to the cart.

### 15. **Products**
   - **Purpose**: The main component that consolidates product listings and filtering functionalities.
   - **Key Features**:
     - Combine `AllProductsSection`, `FiltersGroup`, and `ProductsHeader` to present a cohesive product browsing experience.
     - Manage the state and data flow for product listings.

### 16. **ProductsHeader**
   - **Purpose**: Handles sorting options for products.
   - **Key Features**:
     - Provide sorting options such as price (ascending/descending), popularity, etc.
     - Work in conjunction with the `AllProductsSection` to re-order products based on selected criteria.

### 17. **ProtectedRoute**
   - **Purpose**: Wraps routes that require user authentication, ensuring that only logged-in users can access certain pages.
   - **Key Features**:
     - Redirect unauthenticated users to the `LoginForm` component.
     - Protect sensitive routes like the Cart and Account pages.

### 18. **SimilarProductItem**
   - **Purpose**: Displays similar products based on the product currently being viewed.
   - **Key Features**:
     - Show a list of similar products that may interest the user.
     - Allow quick navigation to similar products from the `ProductItemDetails` page.





## API Endpoints

- **POST** `/login`: Authenticates users and returns a token.
- **GET** `/products`: Fetches a list of all products.
- **POST** `/cart`: Adds an item to the cart.
- **DELETE** `/cart/:id`: Removes an item from the cart.

## Styling

### Quick Tips:

- Use the `line-height` property to set the spacing between lines of text.
- Use the `find()` array method to search for elements in the cart.

### Color Palette:

- **Primary:** `#0b69ff`
- **Secondary:** `#171f46`
- **Text:** `#616e7c`
- **Background:** `#ffffff`

## Resources

- **Icons:** Use `react-icons` for cart item controls.
  - `BsPlusSquare`: Plus button.
  - `BsDashSquare`: Minus button.
  - `AiFillCloseCircle`: Remove button.

## Important Notes

- **Prime User Credentials:** 
  - Username: `rahul`
  - Password: `rahul@2021`

- **Non-Prime User Credentials:** 
  - Username: `raja`
  - Password: `raja@2021`

- Ensure that all components are implemented in the `src/components` directory and maintain the given folder structure.

By following this guide, you should be able to implement the cart features and authentication in your e-commerce application effectively.