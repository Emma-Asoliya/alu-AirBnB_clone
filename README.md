AirBnB Clone - The Console

Description of the Project

The AirBnB Clone project is a comprehensive endeavor to build a complete web application inspired by AirBnB. This first phase focuses on creating a command interpreter (referred to as "the console") that allows developers to manage data and objects within the system. This console serves as the backbone for subsequent phases, including front-end integration, database storage, API development, and HTML/CSS templating.

Features of the Console
- Create new objects, such as User, Place, State, City, and more.
- Retrieve objects stored in a file or database.
- Update attributes of objects.
- Delete objects.
- Serialize and deserialize objects to and from JSON format.

Description of the Command Interpreter

The command interpreter is a shell-like interface that allows users to interact with the AirBnB Clone system. It is built using Python's cmd module and offers a simple and intuitive way to manage objects.

Key Commands
- create <class_name>: Creates a new object and saves it to the file.
- show <class_name> <id>: Retrieves an object by its ID.
- destroy <class_name> <id>: Deletes an object by its ID.
- all [<class_name>]: Displays all objects or objects of a specific class.
- update <class_name> <id> <attribute_name> <attribute_value>: Updates attributes of an object.


How to Start the Command Interpreter

Prerequisites
- Python 3.8.5 or later.
- A terminal or command-line interface.

Steps to Start
1. Clone the repository:
   git clone https://github.com/your_username/alu-AirBnB_clone.git

2. Navigate to the project directory:
   cd alu-AirBnB_clone

3. Run the console in interactive mode:
   ./console.py
   You will see a prompt like this:
   (hbnb)

4. Alternatively, run the console in non-interactive mode:
   echo "<command>" | ./console.py


How to Use the Command Interpreter

Interactive Mode
- Start the console using ./console.py.
- Type commands at the (hbnb) prompt.
- Example:
  $ ./console.py
  (hbnb) create User
  6f6bcd4b-f22c-4c0e-b30b-ff72f2c404ff
  (hbnb) show User 6f6bcd4b-f22c-4c0e-b30b-ff72f2c404ff
  [User] (6f6bcd4b-f22c-4c0e-b30b-ff72f2c404ff) {"id": "6f6bcd4b-f22c-4c0e-b30b-ff72f2c404ff", "created_at": "2025-01-19T12:34:56.789123", "updated_at": "2025-01-19T12:34:56.789123"}
  (hbnb) quit


Non-Interactive Mode
- Execute a single command:
  echo "create User" | ./console.py
 
  Output:
  (hbnb) 6f6bcd4b-f22c-4c0e-b30b-ff72f2c404ff

- Use scripts to run multiple commands:
  echo -e "create User\nshow User 6f6bcd4b-f22c-4c0e-b30b-ff72f2c404ff\nquit" | ./console.py
  

Examples

Creating a New Object
(hbnb) create User
6f6bcd4b-f22c-4c0e-b30b-ff72f2c404ff


Retrieving an Object
(hbnb) show User 6f6bcd4b-f22c-4c0e-b30b-ff72f2c404ff
[User] (6f6bcd4b-f22c-4c0e-b30b-ff72f2c404ff) {"id": "6f6bcd4b-f22c-4c0e-b30b-ff72f2c404ff", "created_at": "2025-01-19T12:34:56.789123", "updated_at": "2025-01-19T12:34:56.789123"}


Updating an Object
(hbnb) update User 6f6bcd4b-f22c-4c0e-b30b-ff72f2c404ff name "John Doe"
(hbnb) show User 6f6bcd4b-f22c-4c0e-b30b-ff72f2c404ff
[User] (6f6bcd4b-f22c-4c0e-b30b-ff72f2c404ff) {"id": "6f6bcd4b-f22c-4c0e-b30b-ff72f2c404ff", "created_at": "2025-01-19T12:34:56.789123", "updated_at": "2025-01-19T12:45:00.123456", "name": "John Doe"}


Deleting an Object
(hbnb) destroy User 6f6bcd4b-f22c-4c0e-b30b-ff72f2c404ff
(hbnb) show User 6f6bcd4b-f22c-4c0e-b30b-ff72f2c404ff
**no instance found**


