1. Return ALL the data in the 'movies' table.

SELECT * FROM movies;

2. Return ONLY the name column from the 'people' table

SELECT name FROM people;

3. Return ONLY your name from the 'people' table.

SELECT name FROM people WHERE name = 'Gregor Gilchrist';

4. The cinema is showing 'Batman Begins', but Batman is DC, not Marvel! Delete the entry from the 'movies' table.

DELETE FROM movies WHERE id = 9;

5. Create a new entry in the 'people' table with the name of one of the instructors.

INSERT INTO people (name) VALUES ('Valerie Dryden');

6. Sadly, Graeme has hurt himself and wont be able to make it, Delete his entry from the 'people' table

DELETE FROM people WHERE (name = 'Graeme Bell');

7. Somehow the list of people includes two people named 'Adam'. Change these entries to the proper names (Jeff 3, Jeff 3.2)

UPDATE people SET name = 'Jeff 3' WHERE id = 15;
UPDATE people SET name = 'Jeff 3.2' WHERE id = 13;

8. The cinema has just heard that they will be holding an exclusive midnight showing of 'Guardians of the Galaxy 2'!! Create a new entry in the 'movies' table to reflect this.

INSERT INTO movies (title, year, show_time) VALUES ('Guardians of the Galaxy 2', 2016, '00.00');

9. The cinema would also like to make the Guardian movies a back to back feature. Update the 'Guardians of the Galaxy' show time from 12:10 to 21:30

UPDATE movies SET show_time = '21.30' WHERE id = 11;

## Extension

1. Research how to delete multiple entries from your table in a single command.

One method is to use 'IN' and then a list of values:
DELETE FROM movies WHERE id IN (1, 2, 3);

'BETWEEN' also works in a similar way to delete consecutive entries (the deletion includes the first and last values given):
DELETE FROM movies WHERE id BETWEEN 1 AND 4;
