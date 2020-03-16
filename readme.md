As of today, 03/03/2020, I am starting this challenge, "33 challenge," until 06/06/2020. I tweaked the “a commit a day” challenge. I will do 3 commits in three days, instead. The difference is, those three commits can be done in any days among three days, not necessarily one per day. Each commit will cover different parts of my workflow, which starts with PostgreSQL or MS SQL Server to extract/load/transform the raw data, then explores data with D3.JS by producing descriptive statistics, and finally generates web map using Leaflet or Openlayer. So there will be one commit for SQL code, one commit for D3.JS, and one commit for Leaflet or other frontend format.


Use this website to see what I am doing day by day. https://dongsoomikeseo.github.io/33challenge/





•	In“Demographic lifestyle” data, add a new column field where sum of population count for desirable lifestyle (8,15,37) is divided by sum of population count for all 50 lifestyle (See appendix 1 for source SQL code). This column represents the percentage of good customers.   
•	Spatial join “Population” data to “Demographic lifestyle” data. While joining, the population count will be summed up by each area in Demographic lifestyle data.
•	Add a new column field where “sum of population is divided by shape area of each area in Demographic lifestyle data. This column will represent population density in each area.    
•	Select areas in Demographic lifestyle data where (the percentage of  good customers is greater than or equal to 10%) and the population density is greater than 0.001. Total 33 areas are selected, out of 260. 
•	Apply 6km buffer to existing store location datasets. If the new location is 6km away from any of existing ones, their 3km coverages would not have any overlapping.
•	Erase the selected areas in Demographic lifestyle data using 6km buffer area. Total 21 areas remain, either intact or partially erased. (See appendix 2 for final output map, and see appendix 3 for the whole model workflow.)
