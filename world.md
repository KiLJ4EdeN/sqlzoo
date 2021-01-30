# Part 1

# World Table

##### simple column select.
```
SELECT population FROM world
```

##### select column with a condition.
```
SELECT population FROM world
  WHERE name = 'France'
```

##### select column with a condition.
```
SELECT population FROM world
  WHERE name = 'France'
```

##### select a bunch of columns.
```
SELECT name, continent, population FROM world
```

##### select a bunch of columns.
```
SELECT name, continent, population FROM world
```

##### column comparison.
```
SELECT name
  FROM world
 WHERE population > 100000000
```

##### column comparison.
```
SELECT name
  FROM world
 WHERE population > 100000000
```

##### combination of features.
```
SELECT name, gdp/population
FROM world
WHERE population > 200000000
```

#### more examples:
```
SELECT name, population/1000000 FROM world
WHERE continent = 'South America'
```

#### IN
```
SELECT name, population FROM world
WHERE name IN ('France', 'Germany', 'Italy')
```

#### CONTAINS
```
SELECT name FROM world
WHERE name LIKE '%United%'
```

#### DOUBLE CONDITION OR
```
SELECT name, population, area FROM world
WHERE area > 3000000 or population > 250000000
```


#### XOR
```
SELECT name, population, area FROM world
WHERE (area > 3000000 and population < 250000000) or 
      (area < 3000000 and population > 250000000)
```

#### ROUND
```
SELECT name, ROUND(population/1000000, 2),
ROUND(gdp/1000000000, 2)
FROM world
WHERE continent = 'South America'
```

#### ROUND REAL NUMBERS ALSO NOT ONLY FRACTIONAL WITH - OPERATOR
```
SELECT name, round(gdp/population, -3) FROM world
WHERE gdp > 1000000000000
```

#### NAME THE EXTRACTED FEATURE
```
SELECT name, round(gdp/population, -3) percapgdp FROM world
WHERE gdp > 1000000000000
```


#### SELECT, LENGTH, AND LIKE REGEX
#### G% startswith
#### %A endswith
```
SELECT name,      LEN(name), 
       continent, LEN(continent),
       capital,   LEN(capital)
  FROM world
 WHERE name LIKE 'G%'
```

#### Also can be named
#### Here we can use "AS"
#### But its preferred to use that only when renaming.
```
SELECT name AS newname,      LEN(name) lname, 
       continent, LEN(continent) lcontinent,
       capital,   LEN(capital) lcapital
  FROM world
 WHERE name LIKE 'G%'
```


#### NOT operator
#### LEFT operator that return the left side character
```
SELECT name, capital
FROM world
WHERE (LEFT(name,1) = LEFT(capital,1)) AND NOT (name = capital)
```

#### QUEST 11
```
SELECT name , capital
  FROM world
 WHERE LEN(name) = LEN(capital)
```

#### USE THE TABLE NAME FOR INDEXING
#### USEFUL WHEN USING MULTIPLE TABLES
```
SELECT name , capital
  FROM world wr
 WHERE LEN(wr.name) = LEN(wr.capital)
```

#### QUEST 13
```
SELECT name
FROM world
WHERE name LIKE '%u%' 
  and name LIKE '%a%' 
  and name LIKE '%o%' 
  and name LIKE '%i%'
  and name LIKE '%e%'
  and name NOT LIKE '% %'
```

