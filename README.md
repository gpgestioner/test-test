# Dpella.io
This repo contains the source code and documentation powering [Dpella.io](https://www.dpella.io/ "Dpella.io")

 **Introduction**  ![](https://img.shields.io/badge/Dpella.io-Demo-success)
 
At DPella, we believe that privacy solutions are increasingly becoming an essential segment of any industry. However, privacy is hard to get right! We’ve only just started, but we already know that every privacy-related-products require to be built around solid mathematical foundations to provide strong guarantees; an aspect that we embrace and we are experts at.

Our solutions are designed to enable your company to perform data analytics on private datasets while respecting the privacy of individuals.

##### Web Interface 
This system has an intuitive interface which allows a simple and attractive navigability, we hope you have a good experience when browsing our site.

### Documentation
<hr>

##### This system runs in visual studio 2019 Community

It is composed of the following technologies:

 ![](https://img.shields.io/badge/Visual%20Studio%202019-IDE%20Community-inactive)
  ![](https://img.shields.io/badge/MVC-architecture%20pattern-success)
  ![](https://img.shields.io/badge/Service%20REST-Web%20Api-success)
 ![](https://img.shields.io/badge/C%23-Backend-green)
 ![](https://img.shields.io/badge/HTML5-HiperText%20Markup%20language-informational)
 ![](https://img.shields.io/badge/CSS-styles-9cf)
 ![](https://img.shields.io/badge/Razor-Markup%20syntax-blue)
 ![](https://img.shields.io/badge/Entity%20Framework-6.x-blue) 
 ![](https://img.shields.io/badge/Newtonsoft%20JSON-12.0.3-blue)
 ![](https://img.shields.io/badge/MvcContrib-2.0.95-blue)
 ![Charts](https://img.shields.io/badge/plotly.com%2Fjavascript-Charts-blue)

Our system is a web service with a web interface, developed in C# language using the .NET Framework platform, which is Microsoft's IDE (Integrated Development Environment).

#####  ¡ IMPORTANT !

To install visual studio 2019 you need to enter here  [Visual Studio 2019 Community](https://visualstudio.microsoft.com/es/thank-you-downloading-visual-studio/?sku=Community&rel=16 "Visual Studio 2019 Community")

Before cloning it, we must have visual studio 2019 Community installed with the following worklands:

<img src="https://i.imgur.com/60gulsO.png" title="source: imgur.com" />

select and install them -> <img src="https://i.imgur.com/7598bSc.png" title="source: imgur.com" />

- **clone the repository **from console, visual studio or sourcetree tool

<img src="https://i.imgur.com/sXdSqD0.png" title="source: imgur.com" />

- verify that the **references** are correctly installed, if everything works correctly you can run it and use the project

- *If it does not work correctly*, what you should do are the following steps:

- check in **Tools** -> **options** -> **Restore packages**, check that the boxes are activated

<img src="https://i.imgur.com/UD99Xjz.png" title="source: imgur.com" />

-  If it shows us the following error when loading the references:

<img src="https://i.imgur.com/3GeXWiS.png" title="source: imgur.com" />

-  Open the nuget package console to run this "Update-Package -reinstall" command, all or most of the references will be loaded, so the main error will go away.
<img src="https://i.imgur.com/IoDL3Se.png" title="source: imgur.com" />

- If nuget couldn´t load all the references, you are probably missing the References to MvcContrib, Entity Framework, Newtonsoft.Json, among the examples. At this point you must open the nuget administrator and install the missing ones one by one (check that the versions are the same)

<img src="https://i.imgur.com/uiileve.png" title="source: imgur.com" />

- Once you have completed these steps, the references will no longer give us an error, we will see the following:

<img src="https://i.imgur.com/QL1cK0U.png" title="source: imgur.com" />

- After that, if the error disappeared we can run the code:
**Running Locally**  **=>** <span style="color: #567;">**Step 4**</span>
-- Run IIS Explorer (your Browser) on your local machine
-- Open http://localhost:XXXX (project port) to open the site in your favorite browser


#### Configuration
<hr>
- This project was started in a .Net Framework MVC 4.6.1 structure, as you have read earlier in this document, implementing that model, we also have within our architecture, we can find the services, which for now we present the logs technique and our connection to the REST api.
- The base configuration of the project is the one created by the developers based on the updates provided by the Dpella api.
- Our Web service is running on a SQL Server

##### REST service
- Remember that this project is connected to the web service to work, for that we need a class that does this serialization. So once you see that the web service is working correctly, our site will have full functionality
- Make the calls to the dpella endpoints, which work with data privacity, receiving the Dataset, Structure and Histogram lists, methods which return a * responseDTO *.

- the process to generate an Analyze in the view is as follows:
 - Enter **Datasets**
 - *Choose a column*
 - Choose the type of **Histogram** *and press continue*
 - You will see that you can perform your *analysis* by calculating the ***epsilon*** and the ***beta*** with the amount of **bins**.

##### Charts of plotly 
![Charts](https://img.shields.io/badge/plotly.com%2Fjavascript-Charts-9cf) [Plotly / Charts Javascript](https://plotly.com/javascript/error-bars/#horizontal-error-bars "Plotly / Charts Javascript")
- We use plotly as a graphics library, which is an open source library that provides what we need to make our graph. Histogram and Error Bar, etc.
