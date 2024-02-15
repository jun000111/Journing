# Journing - Django and JQuery based web application

![GitHub last commit (branch)](https://img.shields.io/github/last-commit/ndh001/Journing/main)

![index](project_imgs/index.png)

## Table of Contents

- [Overview](#Overview)
- [RESTFUL API](#RESTFUL_API)
- [Installation](#Installation)
- [Documentations](#Documentations)
- [Disclaimer](#Disclaimer)

## Overview

An innovative web application developed using the Django framework in conjunction with JQuery, designed to facilitate seamless user interaction with comprehensive travel information - which was pre-scrapped from ctrip.com and are stored in the local postgres database. This platform empowers users to efficiently navigate and explore travel-related data, engage in commentary, establish interconnected communities, and notably, plan and curate individualized travel itineraries.

Deployed on an AWS EC2 web instance using Gunicorn and Nginx, alongside services like RDS (Postgres) and S3.

The webpage encompasses a range of essential functionalities, including but not limited to:

**1. User authentication and registration**
![regi](project_imgs/regi.png)
![login](project_imgs/login.png)

**2. Browse travel information ( Data scrapped from the chinese version of trip.com --> ctrip.com )**
![cities](project_imgs/cities.png)

**3. Establish connection between users**
![connection](project_imgs/connection.png)

**4. View and make comments on attractions or topics**
![comments](project_imgs/comments.png)

**5. Mark attractions/restaurants/shops**
![mark](project_imgs/mark.png)

**6. Customize personal travel plan with the pre-marked collections**
![journal](project_imgs/journal.png)

#### Responsive mobile design

While the project was primarily tailored for desktop users(Google Chrome), it's noteworthy that a significant portion of its features is also accessible through mobile phones, thanks to the implementation of a responsive design. It's important to mention that rigorous testing has been conducted on devices such as the iPhone XR and Oppo R17. Nevertheless, it's essential to acknowledge that this testing does **not** ensure flawless styling across the entire spectrum of mobile devices.
<br>
<img src='project_imgs/m_cities.jpeg' style='width:22%;display:inline;'>
<img src='project_imgs/m_collection.jpeg' style='width:22%;display:inline;'>
<img src='project_imgs/m_detail.jpeg' style='width:22%;display:inline;'>
<img src='project_imgs/m_journal.jpeg' style='width:22%;display:inline;'>

## RESTFUL_API

The website also facilitates the integration of RESTful API calls from external sources, while providing comprehensive CRUD (Create, Read, Update, Delete) capabilities for specific functionalities.

To retrieve data such as attractions, foods, and shops, initiate a GET request to the following endpoint: https://journing.co/api/[category], where [category] can be replaced with either 'sights', 'foods', or 'shops'.

For CRUD operations, the platform supports the manipulation of comments. To authenticate, include either '5134f4b0-f6d6-4cb0-9328-ad6f896bf086' or '3b7746d5-6e56-4f84-952a-ecf914b3487b' in the HTTP request header. Subsequently, utilize the CRUD capabilities by interacting with the endpoint: https://journing.co/api/comments to execute the desired actions.
<br>
<img src="project_imgs/web_api.png" style='width:40%'>
<img src="project_imgs/remote_api.png" style='width:40%'>

## Installation

Follow the installation step and set up the project.

1.  **Clone the Repository:** Begin by cloning this project to your local repository using :
    `git clone https://github.com/NDH001/Journing.git`
2.  **Install Dependencies:** Navigate to the project directory and install the required dependencies by running: `pip install -r requirements.txt`
3.  **Database Migration:** Apply the necessary database migrations with the following command:
    `python manage.py migrate`
4.  **Import Data:** Import the pre-scrapped travel data to the postgres database by running : `psql your_database_name < migrates.sql` ( the csv files are not provided here , please contact me at zhi_jun23@hotmail.com for the csv files)
5.  **Run the Development Server:** Launch the development server using: `python manage.py runserver`

## Documentations

The objective of this segment is to furnish comprehensive elucidation pertaining to the project in question. The documentation encompassing elements such as the product backlog, database schemas, prototyping documents, and the Gantt chart, is enumerated herewith.

**1. Product backlog & Gantt Chart :** The project is founded upon an Agile methodology coupled with the Scrum framework. Each week is designated as a discrete sprint, wherein the activities encompass the stages of application development, thorough review, and rigorous testing. The project encompasses a timeline extending over a duration of three months, commencing with data scraping and subsequently progressing to the substantive phases of application development.
![Backlog](project_imgs/product.png)
![gantt](project_imgs/gantt.png)

**2. Data Scrapping :** The data presented on the website has been sourced through a pre-scraping process from ctrip.com. For those interested in delving into the details of this data acquisition, the corresponding [project](https://github.com/NDH001/travelWeb_scrapper) offers comprehensive source code and step-by-step instructions on how to effectively gather the data utilized within this endeavor.

**3. Database schemas :** The database encompasses four distinct schemas, with each segment dedicated to the storage of pertinent data and content that fall within specific categories. To view the original PDF illustrating this structure, kindly access it by clicking here.
![database](project_imgs/database.png)

**4. Prototye:** This subsection contains some of the initial design and ideas for the website. Click [here](project_imgs/) to view the original images.
<br>
<img src='project_imgs/1.png' style='width:30%;display:inline;'>
<img src='project_imgs/2.png' style='width:30%;display:inline;'>
<img src='project_imgs/3.png' style='width:30%;display:inline;'>
<img src='project_imgs/4.png' style='width:30%;display:inline;'>
<img src='project_imgs/5.png' style='width:30%;display:inline;'>
<img src='project_imgs/6.png' style='width:30%;display:inline;'>
<img src='project_imgs/7.png' style='width:30%;display:inline;'>
<img src='project_imgs/8.png' style='width:30%;display:inline;'>
<img src='project_imgs/9.png' style='width:30%;display:inline;'>

## Disclaimer

This project is strictly non-profit and is solely intended for personal use. All data presented or utilized in this project has been obtained from ctrip.com through legal web scraping methods. The intention behind this project is to showcase technical skills and provide insights derived from publicly available data. No commercial intent or financial gain is associated with this project.

Please note that this project is not affiliated with or endorsed by ctrip.com in any way. The data used is publicly accessible information that has been collected through lawful means. If you are the owner or representative of ctrip.com and have concerns about the usage of this data, please feel free to me at zhi_jun23@hotmail.com, and I will be glad to address any inquiries.
