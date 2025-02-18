# Steps to Set Up and Run a Java Application Using Eclipse:
1. Install an IDE for Java Development:
   
Download and install any Java IDE (Eclipse recommended).
2. Install JDK and JRE:
  
Ensure that JDK (Java Development Kit) and JRE (Java Runtime Environment) are installed.
3. Configure Environment Variables:

Open the Environment Variables window.
Add the JDK bin path to the system’s Path variable.
Example:
C:\Program Files\Java\jdk-14.0.1\bin  
(Replace with the actual installation path of your JDK.)
4. Open Eclipse and Set Up a Java Project:
Launch Eclipse in your designated workspace.
Click New → Java Project and provide a project name.
5. Create a Package:
Inside the src folder, create a new package.
Place all Java files inside this package.
6. Configure Build Path:
Right-click on the project and select Configure Build Path.
Go to the Libraries tab and click Add External JARs.
7. Import CloudSim Libraries:
Extract the Cloudsim.tar file you downloaded.
Import the JAR files from Cloudsim.tar into the external JARs section.
8. Update Package Names in Source Files:
Modify the package name in all source files as needed.
9. Run the Java Application:
Right-click on the project and choose Run As → Java Application.
From the list, select SJF_Scheduler.java and execute the program.
