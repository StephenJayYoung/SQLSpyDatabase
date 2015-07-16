# SQLSpyDatabase

Part One
Describe in English what the following SQL queries do. (Don’t just paraphrase the SQL
into words) Also include the first five rows of the result for each query (or fewer, the
result is smaller), and the total number of rows returned.
1.
(a) SELECT * FROM Agent WHERE agent_id = 55;
(b) SELECT DISTINCT city FROM Agent;
(c) SELECT city FROM Agent;
(d) SELECT first, last FROM Agent WHERE salary > 52000 and salary < 55000;
(e) SELECT sc_level, description FROM Securityclearance;
2.
(a) SELECT name, access_id FROM Mission WHERE mission_status='ongoing'
 AND team_id=14;
(b) SELECT name, access_id FROM Mission M WHERE M.mission_status='ongoing' 
 AND M.team_id=14;
(c) SELECT name, access_id FROM Mission WHERE Mission.mission_status='ongoing'
 AND Mission.team_id=14;
3.
(a) SELECT * FROM Agent A, SecurityClearance S WHERE A.salary = 55262
 AND S.sc_level = 'Majestic';
(b) SELECT * FROM Agent A, SecurityClearance S WHERE A.clearance_id = S.sc_id
 AND A.salary = 55262 AND S.sc_level = 'Majestic';
4.
(a) SELECT A.first, A.last, A.city, A.country FROM Agent A, Languagerel LR,
Language L
 WHERE A.agent_id = LR.agent_id AND LR.lang_id = L.lang_id AND L.language =
'Spanish';
(b) SELECT A1.first, A1.last, A2.first, A2.last FROM Agent A1, Agent A2
 WHERE A1.city = A2.city AND A1.country = A2.country
 AND A1.clearance_id < A2.clearance_id AND A1.salary >= A2.salary;
Part Two
Write a single SQL statement for each of the following queries. Show the first five rows
of the result for each query (or fewer, if the result is smaller) and the number of rows
returned. You should be able to write these SQL queries using only the features covered
in the first lecture notes.
5. List the city, country and salary for agent Lilly Li.
6. List the first and last names of all agents with Secret or Top Secret clearance.
(Your query shouldn’t depend on what clearance IDs are used for these clearance levels.)
7. List the first and last names of all agents who speak at least two languages.
8. List the name and status of all missions that have at least one agent with Majestic
clearance.
Don’t repeat missions in your result.
