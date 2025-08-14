# bitSTore E-commerce Platform

A full-stack e-commerce web application with a Django REST API backend and a React frontend.

---

## LIVE LINK
https://deploy-frontend-ecomerce.onrender.com


## Demo


https://github.com/user-attachments/assets/6521aecf-14ac-49d2-a85d-f25d341ae141




## Technologies Used

### Backend
- Python 3.x
- Django 5.x
- Django REST Framework
- SQLite (default, can be swapped for PostgreSQL/MySQL)
- Pillow (for image handling)
- Other Django packages (see `requirements.txt`)

### Frontend
- React 19.x
- Bootstrap 5
- Axios (API requests)
- React Router DOM
- @paypal/react-paypal-js (PayPal integration)
- Testing Libraries: Jest, React Testing Library

---

## Features

### Backend
- Vendor and Customer registration, login, profile management
- Product CRUD (with images, categories, vendor linkage)
- Product search (by name/description)
- Order and Order Item management
- Customer addresses (multiple per customer)
- Product ratings and reviews
- Authentication (basic, can be extended)
- Profile picture upload for vendors/customers
- Pagination for list endpoints

### Frontend
- Home page with latest/popular products, sellers, categories
- Product search and browse (with pagination)
- Category and vendor pages
- Product detail page (with reviews, related products, vendor info)
- Cart and wishlist (global state via React Context)
- Customer review system
- Responsive UI (Bootstrap + glassmorphism)
- Error handling and loading indicators

---

## Setup Instructions

### Backend

1. **Clone the repository** and navigate to the backend directory:
   ```sh
   cd backend
   ```

2. **Install dependencies**:
   ```sh
   pip install -r requirements.txt
   ```

3. **Apply migrations**:
   ```sh
   python manage.py makemigrations
   python manage.py migrate
   ```

4. **Create a superuser** (optional):
   ```sh
   python manage.py createsuperuser
   ```

5. **Run the development server**:
   ```sh
   python manage.py runserver
   ```

6. **Access the API** at `http://127.0.0.1:8000/`

### Frontend

1. **Navigate to the frontend directory**:
   ```sh
   cd frontend
   ```

2. **Install dependencies**:
   ```sh
   npm install
   ```

3. **Start the development server**:
   ```sh
   npm start
   ```

4. **Access the app** at `http://localhost:3000`

---

## API Endpoints

See backend README for a full list. Highlights:
- `/vendors/`, `/vendor/<id>/`, `/vendor/login/`, `/vendor/register/`
- `/products/`, `/product/<id>/`, `/search/`
- `/categories/`, `/category/<id>/`
- `/customers/`, `/customer/<id>/`, `/customer/login/`, `/customer/register/`
- `/orders/`, `/order/<id>/`, `/orderitem/`
- `/product/<id>/add_review/`
- `/customer-dashboard/<id>/`
- `/vendor-order/<vendor_id>/`
- `/order-status/<order_id>/`

---

## How It Works

- **Authentication:** Login/register via API endpoints.
- **Product Images:** Upload via multipart/form-data.
- **Order Placement:** Create order, then add order items.
- **Profile Pictures:** Upload for vendors/customers.
- **Ratings:** Customers post reviews/ratings.

---

## Project Structure

- backend - Django REST API
  - `main/` - Core app (models, views, serializers, migrations)
  - `backend_api/` - Django project settings
  - `media/` - Uploaded images
- frontend - React app
  - `src/` - Components, contexts, pages

---

## Libraries Used

### Backend
- Django
- djangorestframework
- Pillow

### Frontend
- react
- react-dom
- react-router-dom
- axios
- bootstrap
- @paypal/react-paypal-js
- @testing-library/react, jest-dom, user-event

---

## Notes

- Use Django admin at `/admin/` for direct model management.
- For file uploads, ensure `MEDIA_ROOT` and `MEDIA_URL` are configured.
- For production, configure proper authentication and security.

---

## License

MIT (or specify your license)
