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
