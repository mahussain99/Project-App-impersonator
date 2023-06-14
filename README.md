# Project-App-impersonator

Think about your favorite apps, and pick one that stores your data- like a game that stores scores, an app that lets you post updates, etc. Now in this project, you're going to imagine that the app stores your data in a SQL database (which is pretty likely!), and write SQL statements that might look like their own SQL.

CREATE a table to store the data.
INSERT a few example rows in the table.
Use an UPDATE to emulate what happens when you edit data in the app.
Use a DELETE to emulate what happens when you delete data in the app.


#### /* What does the app's SQL look like? */

CREATE TABLE Gaming_App(
 ID INTEGER PRIMARY KEY
, game_date TEXT
, game_name TEXT
, subscriptions_type TEXT
, High_Score Numeric
, lower_Score Numeric
, account_created TEXT);


INSERT INTO Gaming_App VALUES ( 1, "01-29-2015", "Soccer", "Amex", "550", "120", "YES");

INSERT INTO Gaming_App VALUES ( 2, "04-29-2016", "Football", "Visa", "5850", "1280", "YES");

INSERT INTO Gaming_App VALUES ( 3, "06-19-2017", "Cricket", "Master_Card", "5250", "1220", "YES");

INSERT INTO Gaming_App VALUES ( 4, "09-29-2020", "Running", "Discover", "50", "20", "NO");

INSERT INTO Gaming_App VALUES ( 5, "01-29-2015", "Jumping", "Amex", "450", "320", "YES");

INSERT INTO Gaming_App VALUES ( 6, "03-29-2015", "Basketball", "Amex", "1550", "1120", "NO");

INSERT INTO Gaming_App VALUES ( 7, "04-29-2015", "VollyBall", "Apple", "2550", "3120", "YES");

INSERT INTO Gaming_App VALUES ( 8, "01-29-2005", "Soccer", "Amex", "5509", "1290", "YES");

INSERT INTO Gaming_App VALUES ( 9, "01-29-2015", "Crieket", "Amex", "6650", "5120", "YES");

INSERT INTO Gaming_App VALUES ( 10, "01-29-2015", "Basketball", "Visa", "560", "1600", "YES");


SELECT *
FROM gaming_app;

### /* Update Operator*/

Update gaming_app SET game_name = "Cricket"
where game_name = "Crieket";

SELECT *
FROM gaming_app;
------------------------------------------
Update gaming_app SET game_name = "VolleyBall"
Where game_name = "Vollyball";

SELECT *
FROM gaming_app;
-------------------------------------------

### /* Delete Operator*/

Delete from gaming_app
Where id = 5;

SELECT *
FROM gaming_app;

---------------------------------------------------
### /* Alter Function*/
Alter table gaming_app add Mid_Score Numeric;

INSERT INTO Gaming_App (game_date
, game_name
, subscriptions_type
, High_Score
, lower_Score
, Mid_Score
, account_created) VALUES ( 11, "01-29-2010", "Basketball", "Visa", "560", "1600", "YES");

SELECT *
FROM gaming_app;


