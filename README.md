# DragonLabs Inventory

A modern, responsive inventory management application built with React and Axios, designed to manage products with features like create, read, update, delete (CRUD), filtering, and sorting. The app features a sleek UI with vibrant gradients, smooth animations, and a cohesive design.

## Features
- **Product Management**: Add, edit, and delete products with details like ID, name, description, price, and quantity.
- **Filtering & Sorting**: Search products by ID, name, or description, and sort by any column (ID, name, price, quantity) in ascending or descending order.
- **Responsive Design**: Adapts seamlessly to various screen sizes, from mobile to desktop.
- **Modern UI**: Includes vibrant gradients, hover effects, and micro-interactions for a polished user experience.
- **Real-time Feedback**: Displays loading states, success messages, and error notifications with auto-dismiss after 5 seconds.
- **Tagline Section**: Showcases a branded tagline card with a motivational message and company branding.

## Prerequisites
- **Node.js**: Version 16 or higher.
- **Backend API**: A running API server at `http://localhost:8000` with endpoints for `/products/` (GET, POST, PUT, DELETE).
- **Browser**: A modern web browser (Chrome, Firefox, Safari, etc.).

## Installation
1. **Clone the Repository** (if applicable):
   ```bash
   git clone <repository-url>
   cd dragonlabs-inventory
   ```

2. **Install Dependencies**:
   If using a Node.js project, install the required packages:
   ```bash
   npm install react react-dom axios
   ```

   Alternatively, use CDN links for a standalone setup:
   - React: `https://cdn.jsdelivr.net/npm/react@18.2.0/umd/react.development.js`
   - ReactDOM: `https://cdn.jsdelivr.net/npm/react-dom@18.2.0/umd/react-dom.development.js`
   - Axios: `https://cdn.jsdelivr.net/npm/axios@1.7.7/dist/axios.min.js`
   - Babel: `https://cdn.jsdelivr.net/npm/@babel/standalone@7.25.6/Babel.min.js` (for JSX support)

3. **Set Up Files**:
   Place the following files in your project directory:
   - `src/App.jsx`
   - `src/App.css`
   - `src/TaglineSection.jsx`
   - `src/TaglineSection.css`
   - `index.html` (create a basic HTML file to load the app, see below)

4. **Create `index.html`**:
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <title>DragonLabs Inventory</title>
     <script src="https://cdn.jsdelivr.net/npm/react@18.2.0/umd/react.development.js"></script>
     <script src="https://cdn.jsdelivr.net/npm/react-dom@18.2.0/umd/react-dom.development.js"></script>
     <script src="https://cdn.jsdelivr.net/npm/axios@1.7.7/dist/axios.min.js"></script>
     <script src="https://cdn.jsdelivr.net/npm/@babel/standalone@7.25.6/Babel.min.js"></script>
   </head>
   <body>
     <div id="root"></div>
     <script type="text/babel" src="src/App.jsx"></script>
     <script type="text/babel">
       const root = ReactDOM.createRoot(document.getElementById('root'));
       root.render(<App />);
     </script>
   </body>
   </html>
   ```

5. **Start the Backend API**:
   Ensure your backend API is running at `http://localhost:8000`. The app expects the following endpoints:
   - `GET /products/`: Fetch all products.
   - `POST /products/`: Create a new product.
   - `PUT /products/:id`: Update a product by ID.
   - `DELETE /products/:id`: Delete a product by ID.

6. **Run the Application**:
   If using a Node.js setup with a tool like Vite or Create React App:
   ```bash
   npm start
   ```
   For a standalone setup, serve the files using a local server (e.g., `npx serve` or a similar tool) and access the app at `http://localhost:3000`.

## Usage
1. **View Products**: The product list loads automatically, displaying ID, name, description, price, and quantity.
2. **Add a Product**: Fill out the form in the "Add Product" card and click "Add".
3. **Edit a Product**: Click "Edit" on a product row to populate the form, then click "Update".
4. **Delete a Product**: Click "Delete" on a product row and confirm the action.
5. **Search Products**: Use the search bar to filter products by ID, name, or description.
6. **Sort Products**: Click on column headers (ID, Name, Price, Quantity) to sort in ascending or descending order.
7. **View Tagline**: The tagline card displays a motivational message and branding for DragonLabs.

## File Structure
```
dragonlabs-inventory/
├── src/
│   ├── App.jsx           # Main React component for the inventory app
│   ├── App.css           # Styles for the main component
│   ├── TaglineSection.jsx # Component for the tagline card
│   ├── TaglineSection.css # Styles for the tagline card
├── index.html            # Entry point HTML file
├── package.json          # (Optional) Node.js project configuration
└── README.md             # This file
```

## Styling
The application uses a modern design with:
- **Color Palette**: Vibrant gradients (purple and cyan) with a clean white surface for cards.
- **Animations**: Smooth hover effects, scaling transitions, and fade-in messages.
- **Typography**: Uses the `Inter` font for clarity and professionalism.
- **Responsiveness**: Grid-based layout adapts to screen sizes, with a single-column layout on mobile.

## Notes
- The app assumes a backend API is available at `http://localhost:8000`. Update the `baseURL` in `App.jsx` if your API is hosted elsewhere.
- Ensure CORS is enabled on the backend to allow requests from the frontend.
- The `TaglineSection` component is a static card; extend it as needed for dynamic content.
- For production, use minified CDN scripts (e.g., `react.production.min.js`) and consider a build tool like Vite or Webpack.

## Contributing
Contributions are welcome! Please submit a pull request or open an issue for bugs, features, or improvements.

## License
This project is licensed under the MIT License.

---
*Built with 💜 by DragonLabs*