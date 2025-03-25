# Steps to Set Up and Run a Java Application Using Eclipse: 

# 1. Install an IDE: 
Install any IDE for running Java applications (Eclipse is recommended).

# 2. Install JDK and JRE: 
Ensure you have both the Java Development Kit (JDK) and Java Runtime Environment (JRE) installed.

# 3. Set Up Environment Variables:
Open the Environment Variables window.

Add the jdk\bin path to the system’s Path variable.

Example: 
        If your JDK is installed in C:\Program Files\Java\jdk-14.0.1\bin, add this path.

# 4. Open Eclipse: 
Launch Eclipse and set up your preferred workspace.

# 5. Create a New Java Project:

Click on New → Java Project and give it a name.

# 6. Create a Package:

Inside the src folder, create a package and add all your Java source files to it.

# 7. Configure Build Path:

Right-click on the project → Select Configure Build Path.

Go to the Libraries tab and click on Add External JARs.

# 8. Import CloudSim JAR Files:

Extract the Cloudsim.tar file.

Import the JAR files from the extracted folder into the external JARs.

# 9. Update Package Names:

Ensure all source files have the correct package name.

# 10. Run the Project:

Right-click on the project and select Run As → Java Application.

Choose the SJF_Scheduler.java file from the list and execute it.
