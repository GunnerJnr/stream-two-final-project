# Table of Contents

[Project Name](#project-name)

[Description](#description)

[Testing](#testing)

[Installation](#installation)

[Usage](#usage)

[Contributing](#contributing)

[Credits](#credits)

---

## Project name

Code Institute - Stream 2 Final Project. “Avengers Data Dashboard”

[Back to Table Of Contents](#table-of-contents)

---

## Description

The Avengers data dashboard is just that. It is a dashboard to display different
types of Avengers information in the form of graphs, bar charts, pie charts,
table and more, using technologies such as Flask, DC.js, D3.js, Python, MongoDB
and more. If you would like to see the project brief for a full breakdown of
what I was instructed to do then please refer to the [Project
Brief](ProjectBrief.md) file.

Live version of the Avengers data dashboard is available for viewing on Heroku:
<https://boiling-everglades-31193.herokuapp.com/>

Here is a link for the data I used in my project - CSV Data source:
<https://github.com/fivethirtyeight/data/tree/master/avengers>

[Back to Table Of Contents](#table-of-contents)

---

## Testing

I was trying to think of how unit tests fit into this project so that I could
try to use them to test the dashboard data, I am afraid I came up short on this
occasion, the only way I thought I could of perhaps tested the functionality
would of been to use and test some manual dummy data before using the actual
JSON data, but by the time I realised this, it was too late, and due to lack of
time I did not have time to retract on progress and make some.

I did however spend a lot of time testing the responsive nature of the dashboard
in multiple browsers, and different mobile phones and tablets. This actually led
me too a bug on IOS mobile devices, I realised that I had my media breakpoints
set to a min-width of 400px, the device was actually smaller than this and so
the dashboard was ugly and didn’t render as expected. A few adjustments to the
css solved this issue.

One thing I can also say due to lack of time, I did not have chance to make all
of the actual SVG elements of the charts and graphs responsive, although I think
if I had of had time I would of probably used a javascript approach to redraw
the elements on the browser resize using a function of some sort.

I initially had trouble with the intro.js tooltips also as on mobile devices the
first tooltip no matter where positioned seem to always render off screen, I
managed to solve this by changing the div element the step was set up in and now
it seems to work fine.

I unfortunately ran in to problems with `D3/DC.js` I was hoping to get my bar charts and graphs linked up to the table so that it would filter with the other data. Unfortunately due to time constraints I will not be able to have that feauture right now so I have for now moved the table into its own html page, although that currently now contains a bug where if you run the `intro.js` site introduction it will display as if it was on the dashboard, really the functionality should be removed but I do not have time, so I am documenting the bug. I also wanted to make the charts and graphs responsive theirself, instead of just the container being responsive. I thought the keen dashboard might of helped with this but unfortunately it did not.

[Back to Table Of Contents](#table-of-contents)

---

## Installation

### Running the MongoDB Server

- Firstly, you will need MongoDB installed - [Download MongoDB here if you
    need it](https://www.mongodb.com/download-center?jmp=nav#community)

- You should then simply be able to run this command in a terminal/cmd window

`'mongod --config [PATH]\_mongoDB_data\_config\_mongodb_config.conf'`

**NOTE:** You will need to ammend the path as neccessary to suit where you
extracted the file too.

#### Uploading the data for the database to work

• Run mongoDB by running the command mongod in your Terminal/Command Prompt.

• Leave the prompt running as it is and open another Terminal/Command Prompt
window.

• Copy the csv file to the same location as the directory opened in the second
terminal window.

• Enter the following command:

`'mongoimport  -d avengers -c avengers_project --type csv --file avengers.csv
--headerline'`

• The database created: avengers

• The collection name: avengers_project

• The data type to be uploaded: csv

• The filename: \_csv_data\\avengers.csv

• Treat the first record imported as the field names: --headerline

**NOTE:** It will take a few minutes to upload the data. You will see a progress
indicator in the terminal letting you know how much data has approximately been
uploaded.

#### Running the requirements.txt to install needed packages

For virtualenv to install all files in the requirements.txt file.

1. cd to the directory where requirements.txt is located
1. activate your virtualenv
1. run: `pip install -r requirements.txt` in your shell

![](readme_img/dashboard.png)

[Back to Table Of Contents](#table-of-contents)

---

## Usage

[KeenDashboard](#https://github.com/keen/dashboards)

Click the start tour button in the sites navigation for a full tour on each
element and what you can do with it.

[Back to Table Of Contents](#table-of-contents)

---

## Contributing

Here is a link for the data I used in my project - [CSV Data
source:](https://github.com/fivethirtyeight/data/tree/master/avengers)

[Back to Table Of Contents](#table-of-contents)

---

## Credits

Code Institute

Andrew Flowers (CSV data)

[Back to Table Of Contents](#table-of-contents)

---
