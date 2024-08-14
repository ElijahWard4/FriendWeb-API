FriendWeb-API


https://github.com/user-attachments/assets/5746fd96-57a4-461a-a45a-1c27300edfd4



# Description
FriendWeb-API is a RESTful API designed for managing users, thoughts, and reactions in a social network-style application. It provides endpoints for creating, retrieving, updating, and deleting users and their thoughts, as well as managing friendships and reactions.

## Installation
To get started with FriendWeb-API, follow these steps:

1. Clone the repository:
```bash
git clone https://github.com/ElijahWard4/FriendWeb-API.git 
```

2. Navigate to the project directory:
```bash
cd FriendWeb-API
```

3. Install dependencies:
```bash
npm install
```

## Database Setup
This project uses MongoDB as its database. Make sure you have MongoDB installed and running on your machine.

## Running the Application
You can start the application using the following commands:

- Start the application:
```bash
npm start
```
This command will start the server using Node.js.

- Development mode with auto-reloading:
```bash
npm run dev
```
This command uses Nodemon to automatically restart the server whenever you make changes to the code.

- Seeding the database:
```bash
npm run seed
```
This command will populate the database with initial data using the seed script.

## API Endpoints
The FriendWeb-API provides the following endpoints:

### Users
- GET /api/users: Retrieve all users.
- GET /api/users/:id: Retrieve a single user by its _id and populate their thought and friend data.
- POST /api/users: Create a new user.
- PUT /api/users/:id: Update a user by its _id.
- DELETE /api/users/:id: Remove a user by its _id (including associated thoughts).
- POST /api/users/:userId/friends/:friendId: Add a new friend to a user's friend list.
- DELETE /api/users/:userId/friends/:friendId: Remove a friend from a user's friend list.

### Thoughts
- GET /api/thoughts: Retrieve all thoughts.
- GET /api/thoughts/:id: Retrieve a single thought by its _id.
- POST /api/thoughts: Create a new thought and push the created thought's _id to the associated user's thoughts array field.
- PUT /api/thoughts/:id: Update a thought by its _id.
- DELETE /api/thoughts/:id: Remove a thought by its _id.
- POST /api/thoughts/:thoughtId/reactions: Create a reaction stored in a single thought's reactions array field.
- DELETE /api/thoughts/:thoughtId/reactions/:reactionId: Remove a reaction by the reaction's reactionId.

## Technologies Used
- Express: A minimal and flexible Node.js web application framework.
- Mongoose: An elegant MongoDB object modeling for Node.js.
- Nodemon: A tool that helps develop Node.js applications by automatically restarting the node application when file changes in the directory are detected.

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request or open an issue to improve this project.
