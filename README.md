# sqlzoo
sqlzoo examples


# SQL CHEATSHEET


# 1 - Basics

## custom names are written in {}.
## annotations:
### {COLUMN}: custom column name.
### {TABLE}: custom table name.
### {VALUE}: some value.


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
