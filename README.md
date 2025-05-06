Flight Data Analytics
Welcome to the Flight Data Analytics project! This is a simple app built with Streamlit, MySQL, and Plotly that lets you search for flights and view cool visual analytics about flight data.

What You Can Do with This App
Check Flights:

Choose a source city and a destination city.

See available flights between those cities.

View Analytics:

Airline Frequency: See which airlines have the most flights with a pie chart.

Busy Airports: See which airports are the busiest using a bar chart.

Daily Flight Frequency: Check how many flights are there on each day with a line chart.

What You Need
To run this app, you need:

Python 3.x installed on your machine.

MySQL Database set up with flight data.

Some Python packages that you can install with this command:

bash
Copy
Edit
pip install streamlit mysql-connector-python plotly
How to Set It Up
1. Set Up the Database
First, you need to have a MySQL database with the name flights. Inside the database, you should have a table called flights with columns like Source, Destination, Airline, Route, Dep_Time, Duration, Price, and Date_of_Journey.

The app connects to this database through the dbhelper.py file. If you need to update your database details (like username, password, or database name), you can do so in the DB class inside dbhelper.py.

Here’s where you’ll find the connection settings:

python
Copy
Edit
self.conn = mysql.connector.connect(
    host='127.0.0.1',  # Update this if needed
    user='root',  # Update this with your MySQL username
    password='12345',  # Update this with your MySQL password
    database='flights'  # Make sure this is the correct database name
)
2. Run the Streamlit App
Once your database is ready, open a terminal (or Command Prompt) and run the following command:

bash
Copy
Edit
streamlit run app.py
This will launch the app in your web browser, where you can interact with it!

How to Use the App
Check Flights:

Choose a source and a destination city from the dropdown.

Click the "Search" button to see a list of flights between those cities.

View Analytics:

Airline Frequency: A pie chart shows how many flights each airline operates.

Busy Airports: A bar chart shows the most popular departure airports.

Daily Flight Frequency: A line chart shows how many flights happen on each day.

File Structure
Here’s what you’ll find in the project:

bash
Copy
Edit
/flight-data-visualization-python-sql
│
├── app.py            # The Streamlit app
├── dbhelper.py       # The code that connects to the MySQL database
├── requirements.txt  # List of packages you need to install
├── README.md         # This file
Need Help?
Make sure your MySQL database is running and accessible.

If the app can’t connect to the database, check the database details in dbhelper.py and update them if needed.

If you get any errors about missing packages, make sure you’ve installed all the required Python packages with pip install -r requirements.txt.
