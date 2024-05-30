Lecture App is an online scheduling application designed to help users manage and keep track of their lecture schedules efficiently. This application provides a interface for adding, viewing lecture schedules.

Features
User authentication and authorization
Create, view lecture schedules

Installation
Clone the repository: https://github.com/pranav6799/Mern-2024-Project


Navigate to the project directory: cd server and install npm install

Navigate to the client directory and install client dependencies: cd client  npm install vite@latest

Create a .env file in the root directory of the project and add your environment variables: DATABASE_URL, SECRET-KEY, PORT

Usage
Start the server: npm start
Start the client : npm run dev

Backend Routes 
router.post("/api/v1/user/register", authController.register);
router.post("/api/v1/user/login", authController.login);
router.get(
  "/api/v1/user/getAllInstructor", authController.protect,authController.isAdmin,authController.getAllInstructor);

 
 router.post('/api/v1/course/add',authController.protect,authController.isAdmin,upload.single('photo'), courseController.addCourse)
router.get('/api/v1/course/get', courseController.getAllCourse)



router.post('/api/v1/schedule/add', scheduleController.addSchedule)
router.get('/api/v1/schedule/getSchedule/:id', scheduleController.getSchedule)
router.get('/api/v1/schedule/getUserSchedule/:id', scheduleController.getUserSchedule)
router.post('/api/v1/schedule/checkAvailability',scheduleController.checkAvailable)





Dependencies
Server
"bcrypt": "^5.1.1",
    "cors": "^2.8.5",
    "dotenv": "^16.4.5",
    "express": "^4.19.2",
    "jsonwebtoken": "^9.0.2",
    "mongoose": "^8.2.4",
    "morgan": "^1.10.0",
    "multer": "^1.4.5-lts.1",
    "nodemon": "^3.1.0",
    "react-router-dom": "^6.22.3",
    "react-toastify": "^10.0.5",
    "validator": "^13.12.0"

