# MySQL

SELECT population FROM world
  WHERE name = 'Germany'

SELECT name, population FROM world
  WHERE name IN ('Sweden', 'Norway', 'Denmark');

SELECT name, area FROM world
  WHERE area BETWEEN 200000 AND 250000

SELECT name FROM world
  WHERE name LIKE 'Y%'

SELECT name FROM world
  WHERE name LIKE '%y'

SELECT name FROM world
  WHERE name LIKE '%x%'

SELECT name FROM world
  WHERE name LIKE '%land'

SELECT name FROM world
  WHERE name LIKE 'C%ia'

SELECT name FROM world
  WHERE name LIKE '%oo%'

SELECT name FROM world
  WHERE name LIKE '%a%a%a%'

SELECT name FROM world
 WHERE name LIKE '_t%'
ORDER BY name

SELECT name FROM world
 WHERE name LIKE '%o__o%'

SELECT name FROM world
 WHERE name LIKE '____'

SELECT name, capital, continent
  FROM world
 WHERE name LIKE capital

SELECT name, concat(name, 'town')
  FROM world
 WHERE name LIKE '% city'

SELECT name, continent, population FROM world

SELECT name FROM world
WHERE population >200000000

select name, gdp/population from world
where population >200000000

Select name, population/1000000 from world
  where continent = 'South America'

select name, population From world
where name like 'France','Germany','Italy'

select name from world
where name like 'United%'

select name, population, area from world
where area > 3000000 or population >250000000


Parte #2

SELECT SUM(population)
FROM world

select distinct(continent) from world

select sum(gdp) from world
where continent = 'Africa'
group by continent

select count(name) from world
where area > 1000000

select sum(population) from world
where name in ('Estonia', 'Latvia', 'Lithuania')

select continent, count(name)  from world
group by continent

SELECT continent, COUNT(name) from world
where population >= 10000000
group by continent

select continent from world
group by continent
having sum(population) > 100000000

