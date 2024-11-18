# IN18Labs

# BackEnd (Which performs all CRUD operations)
Step 1: Install the Gradle Plugin for Eclipse
If you don't already have the Gradle plugin installed in Eclipse, you need to install it. Follow these steps to install it:

Open Eclipse IDE.
Go to Help > Eclipse Marketplace.
In the Eclipse Marketplace window, search for Buildship Gradle Integration.
Click Go and then click Install for the Buildship Gradle Integration plugin.
Restart Eclipse once the installation is complete.

Step 2: Import the Gradle Project
Once the Gradle plugin is installed, follow these steps to import your Gradle project into Eclipse:

Open Eclipse IDE.
Go to File > Import.
In the Import wizard, select Gradle > Existing Gradle Project and click Next.
In the Project root directory field, click Browse and select the root directory of your Gradle project (where the build.gradle file is located).
Click Finish.

Step 4: Build the Gradle Project in Eclipse
To ensure that your Gradle project is correctly set up, follow these steps:

Right-click on the project in the Project Explorer.
Select Gradle > Refresh Gradle Project to sync the project with Gradle.
Eclipse will download the necessary dependencies defined in your build.gradle file.

Step 5: Run the Application
To run your Gradle project (Spring Boot, Java application, or any other executable):

5.1: Running a Spring Boot Application
Right-click on your project in the Project Explorer.
Navigate to Run As > Spring Boot App. This will start your Spring Boot application.
Alternatively, you can use Run As > Java Application and select the main class (e.g., com.labs.task.Application or the class that contains the main method).

Step 6: To perform CRUD (Create, Read, Update, Delete) operations on your Spring Boot application using Postman, follow these steps after successfully running your project:

Step 1: Run the Application
Ensure that your Spring Boot application is running properly (e.g., on http://localhost:8080 or another port you've configured). You can do this by:

Running your Spring Boot application using the @SpringBootApplication class (typically Application.java or YourAppName.java).
Verify that the application is running by checking the Eclipse Console for any startup messages, such as:
scss
Copy code
Tomcat started on port(s): 8080 (http) with context path ''
Step 2: Open Postman
Open Postman, which is a popular tool for testing APIs. If you don’t have Postman installed, you can download it from the official website.

Step 3: Create a New Request in Postman
3.1: Create (POST)
To create a new resource (e.g., creating a new user registration), use the POST HTTP method.

Open Postman and click on New Request.
Select the POST method from the dropdown menu next to the URL field.
In the URL field, enter the endpoint for your POST request. For example:
bash
Copy code
http://localhost:8080/api/registrations
Go to the Body tab and select raw as the format. Then choose JSON from the dropdown next to it.
Add the JSON data for the request body. For example:
json
Copy code
{
  "name": "John Doe",
  "email": "john.doe@example.com",
  "dateOfBirth": "1990-05-15",
  "phone": "1234567890",
  "address": "123 Main St"
}
Click Send. If everything is set up correctly, you should get a response back with the newly created resource (e.g., a confirmation with the new ID or status message).
3.2: Read (GET)
To read or retrieve the list of resources or a single resource:

Select the GET method in Postman.

For all records:

bash
Copy code
http://localhost:8080/api/registrations
This will return a list of all registration records.

For a specific record, you can use the ID:

bash
Copy code
http://localhost:8080/api/registrations/{id}
Replace {id} with the actual ID of the registration you want to retrieve, e.g.:

bash
Copy code
http://localhost:8080/api/registrations/1
Click Send to get the response.

3.3: Update (PUT)
To update an existing resource:

Select the PUT method in Postman.
Enter the URL for updating a specific resource:
bash
Copy code
http://localhost:8080/api/registrations/{id}
Replace {id} with the actual ID of the registration you want to update (e.g., 1).
Go to the Body tab and select raw and choose JSON.
Add the updated information in the JSON format. For example:

json
Copy code
{
  "name": "John Smith",
  "email": "john.smith@example.com",
  "dateOfBirth": "1990-05-15",
  "phone": "0987654321",
  "address": "456 Elm St"
}

Click Send to update the record. You should receive a response with the updated data.

3.4: Delete (DELETE)
To delete a resource:
Select the DELETE method in Postman.
Enter the URL for deleting a specific resource:
bash
Copy code
http://localhost:8080/api/registrations/{id}
Replace {id} with the actual ID of the registration you want to delete.
Click Send to delete the resource. You should get a success or error message in the response.
Step 4: Verify CRUD Operations
After performing each operation, check the response body and status code to ensure the operation was successful.
200 OK: for successful retrieval or update.
201 Created: for successful creation.
204 No Content: for successful deletion.
400 Bad Request: if there is an issue with the request (e.g., validation errors).
404 Not Found: if the requested resource doesn’t exist (e.g., for a non-existent id).
Step 5: Example API Endpoints in Postman
Here’s a brief overview of what your API endpoints might look like:

POST /api/registrations – Create a new registration.
GET /api/registrations – Retrieve all registrations.
GET /api/registrations/{id} – Retrieve a specific registration by ID.
PUT /api/registrations/{id} – Update a registration by ID.
DELETE /api/registrations/{id} – Delete a registration by ID.
Step 6: Debugging in Postman
If you encounter any issues:

Check the Console in Postman (View > Show Postman Console) to see the request/response details, including any error messages.
Check the Eclipse Console for your Spring Boot application logs to debug any backend issues (e.g., database connection errors or validation issues).


# FrontEnd (Registration Form)

Step 1: Install Visual Studio Code
If you don't have VS Code installed, you can download and install it from the official website.

Step 2: Open VS Code
Open Visual Studio Code.
If you don't see the Welcome page, you can open the Explorer tab on the left side to view your files.
Step 3: Create a New Project Folder
In VS Code, click on File > Open Folder....
Choose or create a folder where you want to store your HTML and CSS files. For example, create a folder named my-web-project.
Step 4: Create HTML and CSS Files
In the Explorer pane, click on New File (the icon with a page and a plus sign) in your project folder.
Create a new HTML file:
Name it index.html.
Write or paste your HTML code in this file.
Create a new CSS file:
Name it style.css.
Write or paste your CSS code in this file.
Step 5: Link CSS to HTML
To link your CSS file to your HTML, you need to add the following code inside the <head> tag of your index.html file:

html
Copy code
<link rel="stylesheet" type="text/css" href="style.css">
Example index.html with linked CSS:

html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Web Project</title>
    <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
    <h1>Welcome to My Web Project</h1>
    <p>This is a sample web page.</p>
</body>
</html>
Step 6: Install Live Server Extension (Optional but Recommended)
To easily view your HTML file in the browser with live reloading:

Go to the Extensions view in VS Code (you can click the Extensions icon on the left sidebar or press Ctrl+Shift+X).
Search for Live Server.
Click Install to install the Live Server extension by Ritwick Dey.
Step 7: Run Your HTML File
Using Live Server:

After installing the Live Server extension, right-click on your index.html file in the Explorer pane.
Select Open with Live Server.
This will open your index.html file in the default web browser and automatically reload the page whenever you make changes.
Manual Method:

You can also open your index.html directly in a web browser by:
Locating the index.html file in your folder.
Right-clicking and selecting Open With -> Your Preferred Browser (e.g., Chrome, Firefox, etc.).
Alternatively, you can drag and drop the index.html file into the browser window.
Step 8: Edit and View Changes
After running the file, any changes you make to your index.html or style.css will be automatically reflected in the browser (if using Live Server).
If you are not using Live Server, manually refresh the browser page after making changes to see the updates.
Step 9: Debugging in VS Code
You can open the Developer Tools in your browser (usually by pressing F12 or Ctrl+Shift+I) to view any errors in the console if something doesn't work.
In VS Code, you can use the Problems tab or the Terminal to check for issues in your code.
