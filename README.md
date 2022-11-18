# Flight-Weather-Search-Engine
![image](https://user-images.githubusercontent.com/102703087/202589373-db9d2add-30f2-4362-a872-67aaa9f16dfe.png)


# Background and Definition of the business use
Though customers can search the flight information and weather information respectively online, it is not convenient for customers to open different websites and may also be confused with different airlines information. In addition, airlines do not supply detailed real-time flight and weather information to their customers, but some customers may concern about those information.
We aim to design a quick, overall, and brand-exclusive searching engine for airline companies. This searching engine can help customers, airport service staff and airline companies to track the latest flight and weather information, once users fill in their flight numbers.

# Data source specification
Real-Time Flight Data is provided by Aaviationstack API
17K real-time domestic flight data were extracted
Data include information about departure, arrival, airline, flight, aircraft,  etc. 

<ul>
  <li>Real-Time Flight Data is provided by Aaviationstack API</li>
      <ul>
          <li>17K real-time domestic flight data were extracted</li>
              <ul>
                  <li>Data include information about departure, arrival, airline, flight, aircraft,  etc.</li>
              </ul>
      </ul>
  <li>Real-Time Weather Data is provided by CheckWX API</li>
      <ul>
        <li>169 real-time weather information were extracted for 169 domestic airports</li>
        <li>Weather data are displayed in the form of Aviation Routine Weather Report</li>
            <ul>
                <li>Data include: barometer, temperature, visibility, wind, humidity, elevation, etc.</li>
            </ul>
      </ul>
</ul>

# Implemented design choices and the rationale
This project utilized real-time flight and weather data to build an information retrieval system

APIs were selected as the data source since they can provide large size real-time data

![accesstomongo](https://user-images.githubusercontent.com/102703087/202591779-65f49ece-9ca1-45b0-a80c-d843ad13a480.jpg)
![images](https://user-images.githubusercontent.com/102703087/202591839-c1ee6156-b48b-466e-ac9a-a41a02c0523c.png)


  <li><b>Extract & Load</b></li>
      <ul>
          <li>Collected data from APIs using python</li>
          <li>Stored weather data (json objects)  in  MongoDB</li>
          <li>Stored flight data (relational data) in PostgreSQL</li>
      </ul>
  <li><b>Transform</b></li>
      <ul>
        <li>Made data more accessible using Python</li>
        <li>Retrieved data from both databases and built  a warehouse</li>
      </ul>
  <li><b>Search & Retrieve</b></li>
      <ul>
        <li>Designed intuitive web interface pages with flask API and html/css</li>
        <li>Fulfilled search and  retrieve functionality based on data warehouse</li>
      </ul>
</ul>

