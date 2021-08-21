# Point-to-point graph for football table data
A script that takes a 'wide' table of a football season and returns a point-to-point line graph.

![image](https://user-images.githubusercontent.com/69304112/130336648-ae7f8496-b39b-412b-8928-a4d54727c26a.png)



How did Union Berlin - the German capital's "other" team - manage to make it into the Europa League while their rivals from the westside of town only just avoided relegation?

These point-to-point graphs show how much advantage Union got from playing at their "fan-built" stadium - even with barely anyone there.

In fact, no other team bar Eintracht Frankfurt had a more disproportionate home ground advantage.

**About**

Created using Plotly Express, with table data from Soccerway.com.

In this example, it looks at the final 2020-2021 Bundesliga season.

Four custom style functions have been built into the graph function: 'Minimalist' (above), 'Default', 'Pastely', 'LightBlueBack'.

![newplot (5)](https://user-images.githubusercontent.com/69304112/130306831-58551689-2bb1-456d-a38d-50d7d4ea6d95.png)
![newplot (3)](https://user-images.githubusercontent.com/69304112/130306759-74e8ced4-a0f7-4346-94e5-a8b76b12da86.png)
![newplot (4)](https://user-images.githubusercontent.com/69304112/130306757-1e4931be-af19-411f-9c83-1dc02179752a.png)

The first part of the script imports the table CSV (future feature: scraping directly from site) and makes a number of simple calculations (eg goals for per home match).  

The p2pGraph function then creates individual p2p graphs, with two teams able to be highlighted. These two teams are noted as 'home' and 'away' as this function is designed to be be used automatically each matchday to produce p2p graphs for that round's various opponents. These two teams are positioned on top of all the other teams' lines (in other words, they are moved to the bottom of the dataframe table).

Four custom style functions have been built into the graph function: 'Default', 'Minimalist', 'Pastely', 'LightBlueBack'. Access these via the chosen_style variable.


**Notes on subplots:**

The Plotly .go version allows for sub plots. 

The Plotly Express .px version produces individual plots. To display them horizontally, there  is a simple workaround: in a website, use a 1x4 grid (width=240px height=800px).

![image](https://user-images.githubusercontent.com/69304112/130305951-a923e56b-c02b-494f-a53c-ec19f3516f53.png)

