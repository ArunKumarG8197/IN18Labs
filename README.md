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
