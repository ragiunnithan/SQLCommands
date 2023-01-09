Table: trips
+-------------------+------+
| Column Name | Type |
+-------------------+------+
| departure_depot | int |
| arrival_depot | int |
| trips_count | int |
+-------------------+------+
(departure_depot, arrival_depot) is the primary key column for this table.
Each row of this table indicates that there were trips_count trips that departed from
departure_depot and arrived at arrival_depot.
Write an SQL query to report the ID of the depot with the most traffic. The depot with the most
traffic is the depot that has the largest total number of trips that either departed from or arrived
at the depot. If there is more than one depot with the most traffic, report them all.
Return the result table in any order.
The query result format is in the following example.
Example 1:
Input:
trips table:
+-------------------+-----------------+---------------+
| departure_depot | arrival_depot | trips_count |
+-------------------+-----------------+---------------+
| 1 | 2 | 4 |
| 2 | 1 | 5 |
| 2 | 4 | 5 |
+-------------------+-----------------+---------------+
Output:
+------------+
| depot_id |
+------------+
| 2 |
+------------+
Explanation:
depot 1 was engaged with 9 trips (4 departures, 5 arrivals).

depot 2 was engaged with 14 trips (10 departures, 4 arrivals).
depot 4 was engaged with 5 trips (5 arrivals).
The depot with the most traffic is depot 2.
Example 2:
Input:
trips table:
+-------------------+-----------------+---------------+
| departure_depot | arrival_depot | trips_count |
+-------------------+-----------------+---------------+
| 1 | 2 | 4 |
| 2 | 1 | 5 |
| 3 | 4 | 5 |
| 4 | 3 | 4 |
| 5 | 6 | 7 |
+-------------------+-----------------+---------------+
Output:
+------------+
| depot_id |
+------------+
| 1 |
| 2 |
| 3 |
| 4 |
+------------+
Explanation:
depot 1 was engaged with 9 trips (4 departures, 5 arrivals).
depot 2 was engaged with 9 trips (5 departures, 4 arrivals).
depot 3 was engaged with 9 trips (5 departures, 4 arrivals).
depot 4 was engaged with 9 trips (4 departures, 5 arrivals).
depot 5 was engaged with 7 trips (7 departures).
depot 6 was engaged with 7 trips (7 arrivals).
The depots with the most traffic are depots 1, 2, 3, and 4.
