# Part 2

# Nobel Table


#### Q1
```sql
SELECT yr, subject, winner
  FROM nobel
 WHERE yr = 1950
```

#### Q2
```sql
SELECT winner
  FROM nobel
 WHERE yr = 1962
   AND subject = 'Literature'
```

#### Q3
```sql
SELECT winner
  FROM nobel
 WHERE yr = 1962
   AND subject = 'Literature'
```

#### Q4
```sql
SELECT yr, subject FROM nobel
WHERE winner = 'Albert Einstein'
```

#### Q5
```sql
SELECT winner FROM nobel 
WHERE subject = 'Peace' AND yr > 1999
```

#### Q6
```sql
SELECT yr, subject, winner FROM nobel 
WHERE (yr BETWEEN 1980 and 1989) AND (subject = 'Literature')
```
