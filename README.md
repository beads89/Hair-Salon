# Eau Claire's Salon

#### An application that allows the user to log employees and clients of a hair salon.

#### Created By: Brandon Eads

## Technologies Used

* C#
* .NET 5
* NuGet
* ASP.NET Core
* Entity Framework Core
* MySql
* MySql Workbench

## Description

This application allows the user to create a database of employees and clients for a salon. A user is able to create employees and make a note of what they specialize in. They will also be able to see that particular employee's clients and assign or remove clients. The application also allows adding clients by name, a brief description of what their style is and assign them to a stylist, as well as delete them from the database, or move them to a different stylist.


## Setup and Usage Instructions

### Technology Requirements

* Download and install [.NET 5](https://dotnet.microsoft.com/download/dotnet/5.0)
* Download and install a code text editor. Ex: [VS Code](https://code.visualstudio.com/)
* Download, install, and complete setup for [MySql Community Server](https://dev.mysql.com/downloads/file/?id=484914) and [MySql Workbench](https://dev.mysql.com/downloads/file/?id=484391).

### Installation

* Clone [this](https://github.com/beads89/Hair-Salon) repository, or download and open the Zip on your local machine
* Open the HairSalon.Solutions folder in your preferred text editor
* To install required packages, navigate to the terminal and type the following commands:
  - dotnet add package Microsoft.EntityFrameworkCore -v 5.0.0
  - dotnet add package Pomelo.EntityFrameworkCore.MySql -v 5.0.0-alpha.2
  - dotnet add package Microsoft.EntityFrameworkCore.Proxies -v 5.0.0
* Create a file named "appsettings.json" in the HairSalon directory
  - add the following code to the appsettings.json file:
  ```
  {
    "ConnectionStrings": {
        "DefaultConnection": "Server=localhost;Port=3306;database=brandon_eads;uid=root;pwd=[YOUR-PASSWORD-HERE];"
    }
  }
  ```
  - replace [YOUR-PASSWORD-HERE] with your unique MySql password
* Launch the MySql server:
  - In the terminal, run the command "$ mySql -uroot -p[YOUR-PASSWORD-HERE]", replacing [YOUR-PASSWORD-HERE] with your unique MySql password
* To Import the required database:
  - Open MySql Workbench
  - Select your preferred server(default is root)
  - In the "Navigator > Administration" window, select "Data Import/ Restore"
  - In "Import Options", select "Import From Self-Contained File"
  - Navigate to "HairSalon.Solutions/brandon_eads.sql" in the search input
  - Under "Default Schema to be Imported to" select the "New" button
  - Enter "brandon_eads" and click "OK"
  - Navigate to the "Import Progress" tab and click "Start Import" in the bottom right corner of the window
  - Reopen the "Navigator>Schemas" tab, Right click and select "refresh all" to see the imported database
* To Restore, build, and run the project:
  - Navigate to the HairSalon.Solutions/HairSalon folder in the command line or terminal
    - Run the command "dotnet restore" to restore the project dependencies
    - Run the command "dotnet build" to build and compile the project
    - Run the command "dotnet run" to build and compile the project

## Known Bugs

* no known bugs

### License

[MIT License](https://opensource.org/licenses/MIT)
Copyright 2021 Brandon Eads

## Support and contact details

* [Brandon Eads](github.com/beads89) <Brandon181989@hotmail.com>