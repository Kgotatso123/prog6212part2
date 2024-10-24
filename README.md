# prog6212part2

To clone your ASP.NET Core MVC application to your local drive, follow these instructions:



 Prerequisites
Before starting, make sure you have the following installed:
- **Git**: You need Git to clone the repository. Download and install it from [git-scm.com](https://git-scm.com/).
- **Visual Studio** (or Visual Studio Code): Make sure you have Visual Studio with the `.NET Core` and `ASP.NET and web development` workload installed.
- **.NET SDK**: Ensure you have the .NET SDK installed to run your application. You can download it from the [.NET Download page](https://dotnet.microsoft.com/download).

 Clone the Repository
1. Open a Terminal/Command Prompt:
   - On Windows, you can use Git Bash, Command Prompt, or PowerShell.
   - On Mac or Linux, use the built-in Terminal.

2. Navigate to the Desired Directory:
   Use the `cd` command to go to the folder where you want to clone the project. For example, if you want to clone the project in `C:\Projects`, run:
   cd C:\Projects

3. Clone the Repository:
   Use the `git clone` command followed by the URL of your GitHub repository. 
 
4. Navigate to the Cloned Folder:
   After cloning, navigate to the folder using the `cd` command
   
 Open the Project in Visual Studio
1. Open Visual Studio.
2. File → Open → Project/Solution.
3. Browse to the folder where you cloned the repository and select the `.sln` (solution) file. Click Open.

Alternatively, you can open the cloned project directly in Visual Studio Code if you prefer a lightweight editor.

 Restore Dependencies
- In Visual Studio, the dependencies are usually restored automatically. However, you can manually restore them by right-clicking the solution in the Solution Explorer and selecting "Restore NuGet Packages".
- Alternatively, you can run the following command in the terminal at the project directory

 Set Up the Database
If your project uses a database (like SQL Server), ensure you have the database connection string set up in your `appsettings.json` file.

Run Database Migrations** (if applicable):
If the application uses **Entity Framework Core**, you may need to apply database migrations:

1. Open Package Manager Console in Visual Studio (Tools → NuGet Package Manager → Package Manager Console).
   
2. Run the following command to apply migrations:
   
   Update-Database
  
   If you're using the command line instead, you can run:
   
   dotnet ef database update

This step creates the database tables and schema if they do not already exist.

 Build and Run the Application
1. Build the Project:
   - In Visual Studio, click on Build → Build Solution or press `Ctrl + Shift + B`.
   - Alternatively, you can use the command:
     
     dotnet build
    
2. Run the Application:
   - In Visual Studio, click the **Start** button or press `F5`.
   - You can also run it from the terminal using:

     dotnet run

   This should launch the application on `https://localhost:5001` (or another specified port).

Verify the Setup
Once the application is running:
- Access the URL displayed in the output console (usually `https://localhost:5001` or `http://localhost:5000`).
- Test if the core features (like creating and managing claims) work as expected.
  
Tips for Troubleshooting Common Issues
- Missing Dependencies: Make sure all NuGet packages are restored using `dotnet restore` or Visual Studio's NuGet Package Manager.
- Database Errors: Check the connection string in `appsettings.json` and verify that the database server is running.
- Build Errors: If you encounter build errors, ensure that all necessary files were cloned, and no files are missing in the solution.

Additional Git Commands
- Update Local Repository: If the repository has updates, run:
  
  git pull origin main

- Create a New Branch: If you want to create a new branch to work on a feature:

  git checkout -b new-feature

- Stage and Commit Changes:

  git add .
  git commit -m "Describe your changes here"

- Push Changes to GitHub:

  git push origin new-feature
