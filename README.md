# Furniro - Furniture E-commerce Admin Dashboard

A modern admin dashboard for managing furniture products with features like filtering, sorting, and pagination.

## Features

- **Product Management**
  - Create, Read, Update, and Delete (CRUD) operations
  - Real-time product filtering by brand and category
  - Price range filtering
  - Multiple sorting options
  - Pagination with customizable items per page
  - Responsive grid layout

- **User Interface**
  - Modern and clean design
  - Responsive layout for all devices
  - Toast notifications for user feedback
  - Loading states and error handling
  - Modal forms for product operations
  - Interactive hover effects on product cards

- **Backend**
  - RESTful API with Express.js
  - MongoDB database integration
  - Efficient data querying and pagination
  - CORS enabled for secure cross-origin requests
  - Environment variable configuration

## Tech Stack

### Frontend
- React.js
- Tailwind CSS
- React Icons
- React Hot Toast
- Remix Icons

### Backend
- Node.js
- Express.js
- MongoDB
- Mongoose
- CORS
- Dotenv

## Getting Started

### Prerequisites
- Node.js (v14 or higher)
- MongoDB Atlas account or local MongoDB installation
- npm or yarn package manager

### Installation

1. Clone the repository
bash
git clone https://github.com/yourusername/furniro-admin.git
cd furniro-admin

2. Backend Setup
```bash
cd backend
npm install

# Create .env file with the following:
PORT=8000
MONGODB_URI=your_mongodb_connection_string
CORS_ORIGIN=http://localhost:5174
```

3. Frontend Setup
```bash
cd frontend
npm install
```

### Running the Application

1. Start Backend Server
```bash
cd backend
npm run dev
```

2. Start Frontend Development Server
```bash
cd frontend
npm run dev
```

The application will be available at:
- Frontend: `http://localhost:5174`
- Backend: `http://localhost:8000`

## API Documentation

### Products API

#### Get Products
```http
GET /api/v1/products
```
Query Parameters:
- `page` (default: 1)
- `limit` (default: 12)
- `brand` (optional)
- `category` (optional)
- `minPrice` (optional)
- `maxPrice` (optional)
- `sort` (optional: 'price:asc', 'price:desc', 'name:asc', 'name:desc')

#### Create Product
```http
POST /api/v1/products
```
Body:
```json
{
  "name": "Product Name",
  "brand": "Brand Name",
  "category": "Category Name",
  "price": 99.99,
  "description": "Product Description"
}
```

#### Update Product
```http
PUT /api/v1/products/:id
```

#### Delete Product
```http
DELETE /api/v1/products/:id
```

## Project Structure

```
furniro-admin/
├── backend/
│   ├── src/
│   │   ├── app.js
│   │   ├── constants.js
│   │   ├── db/
│   │   ├── models/
│   │   └── index.js
│   ├── package.json
│   └── .env
│
└── frontend/
    ├── src/
    │   ├── components/
    │   ├── pages/
    │   ├── App.jsx
    │   └── main.jsx
    ├── package.json
    └── index.html
```

## Features in Detail

### Product Management
- **Create**: Add new products with name, brand, category, price, and description
- **Read**: View products in a responsive grid layout with pagination
- **Update**: Edit existing product details through a modal form
- **Delete**: Remove products with confirmation toast

### Filtering & Sorting
- Filter products by brand name
- Filter products by category
- Filter products by price range
- Sort products by price (ascending/descending)
- Sort products by name (A-Z/Z-A)

### UI/UX Features
- Responsive design for mobile, tablet, and desktop
- Loading spinners for async operations
- Toast notifications for user feedback
- Modal forms for product operations
- Hover effects on product cards
- Pagination controls

## Error Handling

The application includes comprehensive error handling:
- Backend validation errors
- Network request failures
- Invalid data submissions
- Database operation errors
- User-friendly error messages




