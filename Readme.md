Table: trips


| Column Name | Type |
| --- | --- |
| departure_depot | int |
| arrival_depot | int |
| trips_count | int |


(departure_depot, arrival_depot) is the primary key column for this table.
<br> Each row of this table indicates that there were trips_count trips that departed from
departure_depot and arrived at arrival_depot.</br>

***Problem:*** Write an SQL query to report the ID of the depot with the most traffic. The depot with the most
traffic is the depot that has the largest total number of trips that either departed from or arrived
at the depot. If there is more than one depot with the most traffic, report them all.

<br>Return the result table in any order.</br>
<br>The query result format is in the following example.</br>
<br>Example 1:</br>
<br>Input:</br>
<br>trips table:</br>

| departure_depot | arrival_depot | trips_count |
| --- | --- |--- |
| 1 | 2 | 4 |
| 2 | 1 | 5 |
| 2 | 4 | 5 |

Output:

| depot_id |
| --- |
| 2 |

<br>Explanation:</br>
<br>depot 1 was engaged with 9 trips (4 departures, 5 arrivals).</br>
<br>depot 2 was engaged with 14 trips (10 departures, 4 arrivals).</br>
<br>depot 4 was engaged with 5 trips (5 arrivals).</br>
<br>The depot with the most traffic is depot 2.</br>
<br>Example 2:</br>
<br>Input:</br>
<br>trips table:</br>

| departure_depot | arrival_depot | trips_count |
| --- | --- |--- |
| 1 | 2 | 4 |
| 2 | 1 | 5 |
| 3 | 4 | 5 |
| 4 | 3 | 4 |
| 5 | 6 | 7 |

Output:

| depot_id |
| --- | 
| 1 |
| 2 |
| 3 |
| 4 |

<br>Explanation:</br>
<br>depot 1 was engaged with 9 trips (4 departures, 5 arrivals).</br>
<br>depot 2 was engaged with 9 trips (5 departures, 4 arrivals).</br>
<br>depot 3 was engaged with 9 trips (5 departures, 4 arrivals).</br>
<br>depot 4 was engaged with 9 trips (4 departures, 5 arrivals).</br>
<br>depot 5 was engaged with 7 trips (7 departures).</br>
<br>depot 6 was engaged with 7 trips (7 arrivals).</br>
<br>The depots with the most traffic are depots 1, 2, 3, and 4.</br>



***Answer:***

Please find this in action in fiddle: : https://dbfiddle.uk/zLnqU8aU

![image](https://user-images.githubusercontent.com/23237905/211404480-72a4ab46-4cc8-4514-942e-38f5e5158029.png)

