# Flatdango
#Flatdango Flatiron Movie Theater is open for business! You will be building out an application, Flatdango, that allows a user to purchase movie tickets from the theater.

setup
install json serve by running the code:

npm install -g json-server

To watch the db.json server run the code:

json-server --watch db.json

Test your server by visiting this route in the browser:

  http://localhost:3000/films

Then, open the `index.html` file on your browser to run the application.

Write your code in the `src/index.js` file. The base URL for your API will be
[http://localhost:3000](http://localhost:3000).

##Deliverables

 See the first movie's details, including its **poster, title, runtime,
showtime, and available tickets** when the page loads. The number of
available tickets will need to be derived by subtracting the number of
`tickets_sold` from the theater's `capacity`. use:

  GET /films/1

   Example Response:
   {
     "id": "1",
     "title": "The Giant Gila Monster",
     "runtime": "108",
     "capacity": 30,
     "showtime": "04:00PM",
     "tickets_sold": 27,
     "description": "A giant lizard terrorizes a rural Texas community and a heroic teenager attempts to destroy the creature.",
     "poster": "https://www.gstatic.com/tv/thumb/v22vodart/2157/p2157_v_v8_ab.jpg"
   }

See a menu of all movies on the left side of the page in the `ul#films`
element when the page loads. (_optional_: you can style each film in the list
by adding the classes `film item` to each `li` element.) There is a
placeholder `li` in the `ul#films` element that is hardcoded in the HTML —
feel free to remove that element by editing the HTML file directly, or use
JavaScript to remove the placeholder element before populating the list. 

 GET /films

   Example response:
   [
      {
        "id": "1",
        "title": "The Giant Gila Monster",
        "runtime": "108",
        "capacity": 30,
        "showtime": "04:00PM",
        "tickets_sold": 27,
        "description": "A giant lizard terrorizes a rural Texas community and a heroic teenager attempts to destroy the creature.",
        "poster": "https://www.gstatic.com/tv/thumb/v22vodart/2157/p2157_v_v8_ab.jpg"
      },
      {
        "id": "2",
        "title": "Manos: The Hands Of Fate",
        "runtime": "118",
        "capacity": 50,
        "showtime": "06:45PM",
        "tickets_sold": 44,
        "description": "A family gets lost on the road and stumbles upon a hidden, underground, devil-worshiping cult led by the fearsome Master and his servant Torgo.",
        "poster": "https://www.gstatic.com/tv/thumb/v22vodart/47781/p47781_v_v8_ac.jpg"
      }
   ]

 note: click on each the list of movies to display the image and the availaable number of tickets.
      => once clicked the available number of tickets are less by one or by the the number of tickets bought.