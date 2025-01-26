# IPL Data Analysis API

This repository provides a Flask-based API for analyzing Indian Premier League (IPL) cricket data. It includes several endpoints to retrieve team records, player statistics, and match comparisons. The project processes data from public Google Sheets containing IPL matches and ball-by-ball details.

---

## Features
- **Team Records**: Retrieve overall and team-vs-team records for IPL teams.
- **Player Statistics**: Access batting and bowling records of players.
- **Interactive Endpoints**: Get JSON responses for various queries related to teams and players.
- **Dynamic Data Integration**: Uses data from online Google Sheets for real-time updates.

---

## Folder Structure
. ├── app.py # Flask application entry point ├── ipl.py # Logic for team-based data processing ├── jugaad.py # Core logic for player statistics and data integration


---

## Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/ipl-data-analysis-api.git
   cd ipl-data-analysis-api
   ```
2. Set up a Python virtual environment:
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```
3. Install dependencies:
    ```bash
    pip install flask pandas numpy
    ```
Usage
Run the Flask application:

bash
Copy
Edit
python app.py
Access the API: Open your browser or use tools like Postman to interact with the following endpoints:

/: Returns a "Hello World" message.
/api/teams: Get a list of all IPL teams.
/api/teamvteam: Compare records between two teams.
Query Parameters:
team1 - First team name
team2 - Second team name
/api/team-record: Get a detailed record of a team.
Query Parameter:
team - Team name
/api/batting-record: Get batting statistics for a player.
Query Parameter:
batsman - Player name
/api/bowling-record: Get bowling statistics for a player.
Query Parameter:
bowler - Player name
Data Sources
The application uses public Google Sheets as its data source:

Match Data: Link to IPL matches data
Ball-by-Ball Data: Link to IPL ball-by-ball data
API Example Usage
Get All Teams
bash
Copy
Edit
GET http://127.0.0.1:5000/api/teams
Response:

json
Copy
Edit
{
  "teams": ["Mumbai Indians", "Chennai Super Kings", "Royal Challengers Bangalore", ...]
}
Compare Two Teams
bash
Copy
Edit
GET http://127.0.0.1:5000/api/teamvteam?team1=Mumbai%20Indians&team2=Chennai%20Super%20Kings
Response:

json
Copy
Edit
{
  "total_matches": "36",
  "Mumbai Indians": "19",
  "Chennai Super Kings": "16",
  "draws": "1"
}
Contributing
Contributions are welcome! Please fork the repository and submit a pull request.

License
This project is licensed under the MIT License. See the LICENSE file for details.

css
Copy
Edit

Feel free to modify the repository link and other specific details as needed.






You said:
Provide me all this in one single code.
ChatGPT said:
ChatGPT
Here's the complete README.md code for your GitHub repository:

markdown
Copy
Edit
# IPL Data Analysis API

This repository provides a Flask-based API for analyzing Indian Premier League (IPL) cricket data. It includes several endpoints to retrieve team records, player statistics, and match comparisons. The project processes data from public Google Sheets containing IPL matches and ball-by-ball details.

---

## Features
- **Team Records**: Retrieve overall and team-vs-team records for IPL teams.
- **Player Statistics**: Access batting and bowling records of players.
- **Interactive Endpoints**: Get JSON responses for various queries related to teams and players.
- **Dynamic Data Integration**: Uses data from online Google Sheets for real-time updates.

---

## Folder Structure
. ├── app.py # Flask application entry point ├── ipl.py # Logic for team-based data processing ├── jugaad.py # Core logic for player statistics and data integration

yaml
Copy
Edit

---

## Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/ipl-data-analysis-api.git
   cd ipl-data-analysis-api
   ```
2. Set up a Python virtual environment:

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```
3. Install dependencies:
 ```bash
pip install flask pandas numpy
```

Usage

1. Run the Flask application:

 ```bash
python app.py
```

2. Access the API: Open your browser or use tools like Postman to interact with the following endpoints:

### API Endpoints

#### `/`
- **Description**: Returns a "Hello World" message.

#### `/api/teams`
- **Description**: Get a list of all IPL teams.

#### `/api/teamvteam`
- **Description**: Compare records between two teams.
- **Query Parameters**:
  - `team1` - First team name
  - `team2` - Second team name

#### `/api/team-record`
- **Description**: Get a detailed record of a team.
- **Query Parameter**:
  - `team` - Team name

#### `/api/batting-record`
- **Description**: Get batting statistics for a player.
- **Query Parameter**:
  - `batsman` - Player name

#### `/api/bowling-record`
- **Description**: Get bowling statistics for a player.
- **Query Parameter**:
  - `bowler` - Player name

Data Sources
The application uses public Google Sheets as its data source:

Match Data: Link to IPL matches data
Ball-by-Ball Data: Link to IPL ball-by-ball data
API Example Usage
Get All Teams
 ```bash
GET http://127.0.0.1:5000/api/teams
 ```
Response:
  ```bash
{
  "teams": ["Mumbai Indians", "Chennai Super Kings", "Royal Challengers Bangalore", ...]
}
 ```
Compare Two Teams
 ```bash
GET http://127.0.0.1:5000/api/teamvteam?team1=Mumbai%20Indians&team2=Chennai%20Super%20Kings
 ```
Response:
 ```bash
{
  "total_matches": "36",
  "Mumbai Indians": "19",
  "Chennai Super Kings": "16",
  "draws": "1"
}
```