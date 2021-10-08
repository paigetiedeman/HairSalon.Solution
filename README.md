<div align="center">

[![Language][language-shield]][language-url]
[![Language][languageH-shield]][languageH-url]
[![Language][languageC-shield]][languageC-url]
[![MIT License][license-shield]][license-url]


# Eau Claire's Salon


#### _By Paige Tiedeman_  

<br>

#### This is a C# web application using MySQL databases and Entity to collect a list of Stylists and Clients.  

<br>

  <!-- <img src="HairSalon/wwwroot/img/Table.jpg">   -->
  
</div>

## Technologies Used

* C#
* .NET 5.0
* ASP.NET Core MVC
* MSTest
* HTML 
* Bootstrap
* MySQL Workbench
* Entity

## Description

This web application takes users inputs of items and places them in a UL list using RESTful routing.

## Installation Requirements

* _Clone or download the zip file of this repository to your desktop_
* _Navigate into the top level directory_
* _Open in your code editor_
* _Commit and push your .gitignore file to your repo_
* _Add the file BestRestaurant/appsettings.json and insert the following:_
```
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Port=3306;database=paige_tiedeman;uid=[YOUR-UID];pwd=[YOUR-PASSWORD-HERE];"
  }
}
```
* _Insert your MySQL database and user Id_
* _Make sure to have .NET 5.0 installed_
* _Run `$ dotnet restore` in HairSalon.Solution/HairSalon to install bin & obj folders_



## Steps To Use
* _Launch MySQL Workbench and select "Create new SQL tab for executing queries"_
* _Enter the below into the query window and click 'execute'_
```
CREATE DATABASE IF NOT EXISTS paige_tiedeman;
USE paige_tiedeman;
DROP TABLE IF EXISTS `stylists`;
CREATE TABLE `stylists` (
  `StylistId` int NOT NULL AUTO_INCREMENT,
  `Name` varchar(255) DEFAULT NULL,
  PRIMARY KEY (`StylistId`)
);
DROP TABLE IF EXISTS `clients`;
CREATE TABLE `clients` (
  `ClientId` int NOT NULL AUTO_INCREMENT,
  `Name` varchar(255) DEFAULT NULL,
  `StylistId` int DEFAULT '0',
  PRIMARY KEY (`ClientId`)
);
```
* _In your terminal navigate into ProjectName.Solution/ProjectName_
* _Run `$ dotnet build` to build the site_
* _Run `$ dotnet run` to start the live server_
* _Click either button to add to see all stylists or clients_
* _After clicking add item put in your inputs and hit submit to reveal the stylist list!_

## User Stories

<details>

* As the salon owner, I need to be able to see a list of all stylists.
* As the salon owner, I need to be able to select a stylist, see their details, and see a list of all clients that belong to that stylist.
* As the salon owner, I need to add new stylists to our system when they are hired.
* As the salon owner, I need to be able to add new clients to a specific stylist. I should not be able to add a client if no stylists have been added.
</details>

## Known Bugs

* _N/A_

## License

MIT: See Badge at top for Info  
Copyright (c) 2021 Paige Tiedeman  

## Contact Information

_Paige Tiedeman @ github.com/paigetiedeman_  

[license-shield]: https://img.shields.io/badge/License-MIT-blue
[license-url]: https://opensource.org/licenses/MIT
[language-shield]: https://img.shields.io/badge/Language-C%23-green
[language-url]: https://docs.microsoft.com/en-us/dotnet/csharp/
[LanguageH-shield]: https://img.shields.io/badge/Language-HTML-red
[LanguageH-url]: https://developer.mozilla.org/en-US/docs/Web/HTML
[LanguageC-shield]: https://img.shields.io/badge/Language-CSS-blueviolet
[LanguageC-url]: https://developer.mozilla.org/en-US/docs/Web/CSS