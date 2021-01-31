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
SELECT yr, subject FROM nobel
WHERE winner = 'Albert Einstein'
```

#### Q4
```sql
SELECT winner FROM nobel 
WHERE subject = 'Peace' AND yr > 1999
```

#### Q5
```sql
SELECT yr, subject, winner FROM nobel 
WHERE (yr BETWEEN 1980 and 1989) AND (subject = 'Literature')
```

#### Q6
```sql
SELECT * FROM nobel
 WHERE subject = 'Peace'
  AND winner IN ('Theodore Roosevelt',
                  'Woodrow Wilson',
                  'Jimmy Carter',
                  'Barack Obama')
```

#### Q7
```sql
SELECT winner FROM nobel
WHERE winner LIKE 'John %'

SELECT winner FROM nobel nb
WHERE nb.winner LIKE 'John %'
```

#### Q8
```sql
SELECT * FROM nobel
WHERE (yr = 1980 and subject = 'Physics') or (yr = 1984 and subject = 'Chemistry')
```

#### Q9
```sql
SELECT * FROM nobel
WHERE yr = 1980 AND NOT (subject = 'Chemistry' OR subject = 'Medicine')
```

#### Q10
```sql
SELECT * FROM nobel 
WHERE (yr < 1910 and subject = 'Medicine')
OR    (yr >= 2004 and subject = 'Literature')
```

#### Q11
```sql
SELECT * FROM nobel
WHERE winner LIKE 'PETER GR%'

SELECT * FROM nobel
WHERE winner LIKE '%PETER GRÜNBERG%'
```


#### Q12
```sql
SELECT * FROM nobel
WHERE winner LIKE 'EUGENE O''NEILL'
```

#### Q13
```sql
SELECT winner, yr, subject FROM nobel
WHERE winner LIKE 'Sir%'
ORDER BY yr DESC, winner
```

#### Q14
```sql
SELECT winner, subject FROM nobel
WHERE yr = 1984
ORDER BY 
CASE WHEN subject IN ('Physics', 'Chemistry') THEN 1 ELSE 0 END,
subject, winner
```
