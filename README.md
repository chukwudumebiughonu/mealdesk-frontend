# MealDesk: Advanced Food Ordering and Restaurant Management Platform

## About the Project

MealDesk is a comprehensive food ordering and restaurant management Software as a Service (SaaS) platform built with React for the frontend and Express.js for the backend. It empowers users to order food from various restaurants, while allowing restaurant owners to manage their menus, track orders, and handle deliveries.

👉 [Live Demo] [<!-- Add your live demo link here -->
](https://mealdesk-frontend.onrender.com/)
## Key Features:

* **Secure Authentication**: Robust authentication system using Auth0 for both customers and restaurant owners.
* **Restaurant Management**: Restaurant owners can create and manage their restaurant profiles, menus, and orders.
* **User Profiles**: Customers can create and manage their profiles, including delivery addresses.
* **Restaurant Search**: Users can search for restaurants based on location, cuisine, and other filters.
* **Menu Browsing**: Detailed menu viewing for each restaurant with item descriptions and prices.
* **Order Placement**: Seamless order placement process with cart management.
* **Payment Integration**: Secure payment processing using Stripe.
* **Order Tracking**: Real-time order status updates for both customers and restaurant owners.
* **Responsive Design**: Consistent user experience across desktop, tablet, and mobile platforms.

## Tools and Technology

### Frontend:
* **React**
* **TypeScript**
* **React Query**
* **React Hook Form**
* **Zod**
* **TailwindCSS**
* **Shadcn/ui**

### Backend:
* **Express.js**
* **MongoDB**
* **Mongoose**
* **Auth0**
* **Stripe**
* **Cloudinary**

## Detailed Feature Breakdown

1. Authentication:
   * Auth0 integration for secure user authentication
   * JWT token-based authorization
   * User role management (customer, restaurant owner)

2. User Management:
   * User profile creation and editing
   * Address management for delivery

3. Restaurant Management:
   * Restaurant profile creation and editing
   * Menu management (add, edit, remove items)
   * Order management and status updates

4. Restaurant Search and Browsing:
   * Search functionality with filters (cuisine, location)
   * Detailed restaurant view with menu items

5. Order Process:
   * Shopping cart functionality
   * Checkout process with address selection
   * Stripe integration for payment processing

6. Order Tracking:
   * Real-time order status updates
   * Order history for customers and restaurants

7. Image Upload:
   * Cloudinary integration for restaurant and menu item images

8. Responsive Design:
   * Mobile-friendly interface using TailwindCSS

## Backend API Structure

1. User Routes (`/api/my/user`):
   * GET: Fetch current user details
   * POST: Create new user
   * PUT: Update user details

2. Restaurant Routes (`/api/my/restaurant`):
   * GET: Fetch restaurant details
   * POST: Create new restaurant
   * PUT: Update restaurant details
   * GET `/order`: Fetch restaurant orders
   * PATCH `/order/:orderId/status`: Update order status

3. Public Restaurant Routes (`/api/restaurant`):
   * GET `/:restaurantId`: Fetch specific restaurant details
   * GET `/search/:city`: Search restaurants in a city

4. Order Routes (`/api/order`):
   * GET: Fetch user's orders
   * POST `/checkout/create-checkout-session`: Create Stripe checkout session
   * POST `/checkout/webhook`: Handle Stripe webhook events

## Frontend Component Structure

1. Layout Components:
   * Header
   * Footer
   * MainNav
   * MobileNav

2. Page Components:
   * HomePage
   * SearchPage
   * DetailPage (Restaurant Details)
   * OrderStatusPage
   * UserProfilePage
   * ManageRestaurantPage

3. Form Components:
   * UserProfileForm
   * ManageRestaurantForm

4. Utility Components:
   * SearchBar
   * PaginationSelector
   * LoadingButton

## Data Flow

1. User actions in the frontend components trigger API calls using custom hooks (e.g., `useCreateMyRestaurant`, `useGetMyUser`).
2. These hooks use React Query for data fetching and caching.
3. API requests are sent to the backend Express.js server.
4. The backend processes requests, interacts with the MongoDB database using Mongoose models, and returns responses.
5. The frontend updates its state based on the responses, providing real-time updates to the user interface.

