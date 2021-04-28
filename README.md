# World

1. Using COUNT, get the number of cities in the USA.
   
   Input:
   
   SELECT COUNT(Name) FROM city WHERE CountryCode = 'USA';
   
   Output:
   
   ![image](https://user-images.githubusercontent.com/82821693/116386530-c81a2880-a811-11eb-8113-ecaea76ae0f0.png)
   
2. Find out the population and life expectancy for people in Argentina.

   Input:
   
   SELECT Population, LifeExpectancy FROM country WHERE Name = 'Argentina';
   
   Output:
   
   ![image](https://user-images.githubusercontent.com/82821693/116386421-a6b93c80-a811-11eb-9d89-8eb26d65e86c.png)

3. Using IS NOT NULL, ORDER BY, and LIMIT, which country has the highest life expectancy?

   Input:
   
   SELECT Name FROM country WHERE LifeExpectancy IS NOT NULL ORDER BY LifeExpectancy DESC LIMIT 1;
   
   Output:
   
   ![image](https://user-images.githubusercontent.com/82821693/116387389-ad947f00-a812-11eb-8af0-073922d84c44.png)

4. Using JOIN ... ON, find the capital city of Spain.

   Input:
   
   SELECT city.Name FROM city INNER JOIN country ON city.ID = country.Capital WHERE country.Name = 'Spain';
   
   Output:
   
   ![image](https://user-images.githubusercontent.com/82821693/116391864-973cf200-a817-11eb-9bab-a0d1fa9458c3.png)


5. Using JOIN ... ON, list all the languages spoken in the Southeast Asia region.

   Input:

   SELECT DISTINCT countrylanguage.Language FROM countrylanguage INNER JOIN country ON countrylanguage.CountryCode = country.Code WHERE country.Region = 'Southeast Asia';
   
   Output:
   
   ![image](https://user-images.githubusercontent.com/82821693/116390035-8e4b2100-a815-11eb-9ed3-6fc94a58a86d.png)
   
6. Using a single query, list 25 cities around the world that start with the letter F.

   Input:
   
   SELECT Name FROM city WHERE Name LIKE 'F%' LIMIT 25;
   
   Output:
   
   ![image](https://user-images.githubusercontent.com/82821693/116392774-c2741100-a818-11eb-8e22-194e4099b4b5.png)

