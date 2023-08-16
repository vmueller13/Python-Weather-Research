# Python API
<ins>Project Overview</ins>
-----


This challenge uses data to definitively answer and prove the answer to the question "What is the weather like as we approach the equator?". Split into two deliverables, WeathPy and VacationPy, this project seeks to create plots to showcase the relationship between weather variables and latitude and use this information to plan future vacations.

<ins>Processes and Technologies</ins>
-----

*WeatherPy*

For WeatherPy I used the OpenWeatherMap API key to call the information I needed and the Geoapify key for VacationPy. Note: Remember to store your personal information for the API call in a `.gitignore` file so that you do not incur any extra charges. I then generated a cities list using the `citypy` library and created plots to show the relationship between different weather variables and latitude as well as calculating the linear regression and r-value of these comparisons as well.
![Figure 2](WeatherPy_VacationPy/output_data/Fig2.png)
![Figure 4](WeatherPy_VacationPy/output_data/Fig4.png)

*VacationPy*
For the second deliverable, I loaded in the csv that I had created in the first deliverable to a map that showed the size of the point as the humidity in each city. I narrowed down the cities to fit my parameters of temperature between 70-90 degrees and less than 50% humidity. Lastly, I searched for a hotel in each city and mapped them with hover text to give information about the location.
![Figure 5](WeatherPy_VacationPy/output_data/Fig5.png)

<ins>Challenges</ins>
-----
  

The biggest challenge that I faced in this project was using the Geoapify API to find the first hotel located within 10,000 metres of my coordinates. The first few time I ran the code, I wasn't getting any hotels returned in the list. After consulting the documentation online for the API, I realized that I needed to  edit my code as follows:
`# Add filter and bias parameters with the current city's latitude and longitude to the params dictionary
    params["filter"] = f"circle:{lon},{lat},{radius}"
    params["bias"] = f"proximity:{lon},{lat}"`
    
  In working on this challenge, I consulted with my bootcamp students Saroja Shrestha and Kimberly Reitema. as well as the documentation online for `hvplot`, `matplotlib` and `scipy.stats`.
