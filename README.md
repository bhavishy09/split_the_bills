
spilt_the_bills is a full-stack web application designed to simplify group expense tracking and settlement. Whether you're managing trip expenses, shared household costs, or any group-related finances, spilt_the_bills provides an intuitive platform to keep everything organized.

🌐 Live Demo


🚀 Features
User Authentication: Secure sign-up and login functionalities to protect user data
Group Management: Create and manage groups with unique join codes for collaborative expense tracking
Expense Tracking: Add, edit, and categorize expenses within groups for clear financial oversight
Settlement Calculations: Automated calculations to determine who owes whom, simplifying the settlement process
Responsive Design: Optimized for various devices, ensuring a seamless experience on desktops, tablets, and mobile phones
🛠️ Tech Stack
Frontend: React.js
Backend: Node.js, Express.js
Database: MongoDB
Authentication: JWT (JSON Web Tokens)
Deployment: Render
📂 Project Structure


SplitEase2/
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   └── server.js
├── frontend/
│   ├── public/
│   └── src/
│       ├── components/
│       ├── pages/
│       ├── services/
│       └── App.js
├── .gitignore
├── package.json
└── README.md



🧰 Prerequisites
Ensure you have the following installed:

Node.js (v14 or higher)
MongoDB (local installation or MongoDB Atlas)
Git
⚙️ Installation
Clone the repository:

git clone https://github.com/relan1997/spilt_the_bills.git
cd spilt_the_bills
Set up the backend:

cd backend
npm install
Set up the frontend:

cd ../frontend
npm install
🔧 Environment Configuration
Create a .env file in the backend directory and add the following:

PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
NODE_ENV=development
Replace your_mongodb_connection_string and your_jwt_secret_key with your actual values:

For local MongoDB: mongodb://localhost:27017/splitease2
For MongoDB Atlas: Use your cluster connection string
Generate a secure JWT secret (32+ characters recommended)
🚀 Running the Application
Development Mode
Start the backend server:

cd backend
npm run dev
The backend will run on http://localhost:5000

Start the frontend development server:

cd frontend
npm start
The frontend will run on http://localhost:3000

Access the application:

Open your browser and navigate to http://localhost:3000

Production Mode
Build the frontend:

cd frontend
npm run build
Start the production server:

cd backend
npm start
📡 API Endpoints
Authentication
POST /api/auth/register – Register a new user
POST /api/auth/login – Login with existing credentials
POST /api/auth/logout – Logout user
GET /api/auth/me – Get current user profile
Groups
POST /api/groups – Create a new group
GET /api/groups – Retrieve all groups for the authenticated user
GET /api/groups/:id – Retrieve a specific group by ID
PUT /api/groups/:id – Update group details
DELETE /api/groups/:id – Delete a group
POST /api/groups/:id/join – Join a group using join code
Expenses
POST /api/groups/:groupId/expenses – Add a new expense to a group
GET /api/groups/:groupId/expenses – Retrieve all expenses for a group
PUT /api/expenses/:id – Update an expense
DELETE /api/expenses/:id – Delete an expense
GET /api/groups/:groupId/settlements – Get settlement calculations for a group
🎯 Usage
Create an Account: Sign up with your email and password
Create or Join Groups: Start a new group or join existing ones using join codes
Add Expenses: Record shared expenses with details like amount, description, and participants
Track Settlements: View automated calculations showing who owes whom
Settle Up: Mark settlements as complete when payments are made
🧪 Testing
Run tests for both frontend and backend:

# Backend tests
cd backend
npm test

# Frontend tests
cd frontend
npm test
🚢 Deployment
The application is configured for deployment on Render. For other platforms:

Build the frontend: npm run build in the frontend directory
Set environment variables on your hosting platform
Deploy the backend with the built frontend assets
🐛 Troubleshooting
Common Issues:

MongoDB Connection Error: Ensure MongoDB is running and the connection string is correct
Port Already in Use: Change the PORT in your .env file or kill the process using the port
JWT Authentication Fails: Verify your JWT_SECRET is set correctly
CORS Issues: Check that frontend and backend URLs match your configuration
🤝 Contributing
Contributions are welcome! Please follow these steps:

Fork the repository
Create a feature branch:
git checkout -b feature/your-feature-name
Make your changes and commit:
git commit -m 'Add: your feature description'
Push to your branch:
git push origin feature/your-feature-name
Open a Pull Request
Development Guidelines
Follow the existing code style and conventions
Write clear commit messages
Add tests for new features
Update documentation as needed
Ensure all tests pass before submitting
📄 License
This project is licensed under the MIT License.

Made with ❤️ for easier expense sharing
