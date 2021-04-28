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
   
   SELECT city.Name FROM city JOIN country ON city.ID = country.Capital WHERE country.Name = 'Spain';
   
   Output:
   
   ![image](https://user-images.githubusercontent.com/82821693/116391864-973cf200-a817-11eb-9bab-a0d1fa9458c3.png)


5. Using JOIN ... ON, list all the languages spoken in the Southeast Asia region.

   Input:

   SELECT DISTINCT countrylanguage.Language FROM countrylanguage JOIN country ON countrylanguage.CountryCode = country.Code WHERE country.Region = 'Southeast Asia';
   
   Output:
   
   ![image](https://user-images.githubusercontent.com/82821693/116390035-8e4b2100-a815-11eb-9ed3-6fc94a58a86d.png)
   
6. Using a single query, list 25 cities around the world that start with the letter F.

   Input:
   
   SELECT Name FROM city WHERE Name LIKE 'F%' LIMIT 25;
   
   Output:
   
   ![image](https://user-images.githubusercontent.com/82821693/116392774-c2741100-a818-11eb-8e22-194e4099b4b5.png)
   
7. Using COUNT and JOIN ... ON, get the number of cities in China.

   Input:
   
   SELECT COUNT(city.Name) FROM city JOIN country ON country.Code = city.CountryCode WHERE country.Name = 'China';
   
   Output:
   
   ![image](https://user-images.githubusercontent.com/82821693/116394361-bbe69900-a81a-11eb-99dd-4f9d32d6fbd2.png)

8. Using IS NOT NULL, ORDER BY, and LIMIT, which country has the lowest population? Discard non-zero populations.

   Input:
   
   SELECT Name FROM country WHERE Population IS NOT NULL AND Population > 0 ORDER BY Population ASC LIMIT 1;
   
   Output:
   
   ![image](https://user-images.githubusercontent.com/82821693/116394744-36afb400-a81b-11eb-904b-df246258cb70.png)
   
9. Using aggregate functions, return the number of countries the database contains.

   Input:
   
   SELECT DISTINCT COUNT(Name) FROM country;
   
   Output:
   
   ![image](https://user-images.githubusercontent.com/82821693/116395185-b5a4ec80-a81b-11eb-8c16-f43a90d8b800.png)

10. What are the top ten largest countries by area?

    Input:
   
    SELECT Name FROM country ORDER BY SurfaceArea DESC LIMIT 10;
   
    Output:
   
    ![image](https://user-images.githubusercontent.com/82821693/116395489-192f1a00-a81c-11eb-880c-4cb815e7566a.png)
    
11. List the five largest cities by population in Japan.

    Input:
    
    SELECT Name FROM city WHERE CountryCode = 'JPN' ORDER BY Population DESC LIMIT 5;

    Output:
    
    ![image](https://user-images.githubusercontent.com/82821693/116395971-affbd680-a81c-11eb-841b-569df4fcedaf.png)
