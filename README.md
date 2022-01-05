# NodeJS Booking App
An appointment booking client application made using Node JS, Firebase for Login, React framework and Bootstrap for Styling. This application makes use of the Google Calendar API to create appointment timeslots on Google Calender through the server. 

<h2>Requirements:</h2>
<ul> 
  <li>Node</li>
  <li>Server App</li>
</ul>

<h2>Application contents:</h2>

<h3>api</h3>
<ul> 
  <li><b>apibooking.js</b> - A folder containing an instance of axios to make XMLHttpRequests from the browser.</li>
</ul>

<h3>components</h3>
<ul>
  <li><b>Form.js</b> - Our main form for data input, it renders the timeslot.js depending on the date selected from the react-calendar. Uses apibooking.js post method "/book" to post the appointment to the server, after which it refreshes the date upon submit. On each date change the data is updated through the react useState hook. Users logged in Email address is sent through the api call as well as an additional message available to be put through the input field. On a successful message from the server a success message is displayed for a few seconds on the FE. Styled with Bootstrap.</li>
  <li><b>Header.js</b> Styled header with logout button to signout from Firebase</li>
  <li><b>TimeSlot.js</b> -  Provides functionality, checking the date passed to it and making a call through the apibooking.js get method "/timeslots" to check available times from the servers, renders the returned data with a function to adjust the timezone since server serves UTC data</li>
    <li><b>styles.css</b> -  Contains .react-calendar__navigation background color</li>
</ul>
  
<h3>App Working Directory</h3>
<ul>
  <li><b>App.js</b> - Contains the placement for the router and all routes using react-router-dom wrapped with AuthProvider to have global user state managment</li>
  <li><b>Auth.js</b> -  Provides a global state hook for user managment with onAuthStateChanged and react useState</li>
  <li><b>configfb.json</b> - config.json file used with firebase. Generated for a firebase web project</li>
  <li><b>Home.js</b> - Main page of our App containing conditional rendering for either serving the login and signup links or the actual main page of the App</li>
  <li><b>index.js</b> - Root of the application, instances the App</li>
  <li><b>Login.js</b> - Login page. Using firebases signInWithEmailAndPassword has redirecting to the main page in case currentUser gets logged in. Styled with Bootstrap.</li>
  <li><b>SignUp.js</b> - Sign in page. Using firebases createUserWithEmailAndPassword has redirecting to the main page in case currentUser gets logged in. Styled with Bootstrap.</li>
  <li><b>styles.css</b> -  Sets margins to 0 for unwanted spacing</li>

</ul>

Installation and Usage
----------------------
<h3>Instructions:</h3>
<ol>
  <li>setup the Server following the server <i>Readme.md</i></li>
  <li>npm install</li>
  <li>npm start</li>
</ol>

<h3>Usage:</h3>
<ol>
  <li>Register or login using your email</li>
  <li>Select a date, select one of the available time slots. click the book button.</li>
  <li>Check your server Calendar API google account to see the appointment</li>

   
</ol>