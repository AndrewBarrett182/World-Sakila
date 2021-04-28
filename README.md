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
    
12. List the names and country codes of every country with Elizabeth II as its Head of State. You will need to fix the mistake first!

    Input:
    
    SELECT Name, Code FROM country WHERE HeadOfState = 'Elisabeth II';
    
    Output:
    
    ![image](https://user-images.githubusercontent.com/82821693/116396522-69f34280-a81d-11eb-8a97-989e8d5907be.png)

13. List the top ten countries with the smallest population-to-area ratio. Discard any countries with a ratio of 0.

    Input:
    
    SELECT Name, Population / SurfaceArea AS 'Population to Area Ratio' FROM country WHERE (Population / SurfaceArea) > 0 ORDER BY (Population / SurfaceArea) ASC LIMIT 10;
    
    Output:
    
    ![image](https://user-images.githubusercontent.com/82821693/116397568-a5424100-a81e-11eb-974f-3bb56a722e04.png)

14. List every unique world language.

    Input:
    
    SELECT DISTINCT Language FROM countrylanguage;
    
    Output:
    
    ![image](https://user-images.githubusercontent.com/82821693/116413670-c0697c80-a82f-11eb-9342-9fff65903709.png)

15. List the names and GNP of the world's top 10 richest countries.

    Input:
    
    SELECT Name, GNP FROM country ORDER BY GNP DESC LIMIT 10;
    
    Output:
    
    ![image](https://user-images.githubusercontent.com/82821693/116398337-9445ff80-a81f-11eb-8663-6a9575f76e0d.png)

16. List the names of, and number of languages spoken by, the top ten most multilingual countries.

    Input:
    
    SELECT country.Name, COUNT(countrylanguage.Language) FROM countrylanguage JOIN country ON countrylanguage.CountryCode = country.Code GROUP BY country.Name ORDER BY COUNT(countrylanguage.Language) DESC LIMIT 10;
    
    Output:
    
    ![image](https://user-images.githubusercontent.com/82821693/116399226-978dbb00-a820-11eb-8a24-2718b34dfb27.png)

17. List every country where over 50% of its population can speak German.

    Input:
    
    SELECT country.Name FROM country JOIN countrylanguage ON country.Code = countrylanguage.CountryCode WHERE countrylanguage.Percentage > 50 AND countrylanguage.Language = 'German';
    
    Output:
    
    ![image](https://user-images.githubusercontent.com/82821693/116399892-5053fa00-a821-11eb-95b8-032655b79969.png)
    
18. Which country has the worst life expectancy? Discard zero or null values.

    Input:
    
    SELECT Name FROM country WHERE LifeExpectancy IS NOT NULL AND LifeExpectancy > 0 ORDER BY LifeExpectancy ASC LIMIT 1;
    
    Output:
    
    ![image](https://user-images.githubusercontent.com/82821693/116400157-a163ee00-a821-11eb-8ece-b412b7ad9b82.png)

19. List the top three most common government forms.

    Input:
    
    SELECT DISTINCT GovernmentForm, COUNT(GovernmentForm) FROM country GROUP BY GovernmentForm ORDER BY COUNT(GovernmentForm) DESC LIMIT 3;
    
    Output:
    
    ![image](https://user-images.githubusercontent.com/82821693/116412455-9ebbc580-a82e-11eb-8c11-3bda330799c6.png)

20. How many countries have gained independence since records began?

    Input:
    
    SELECT COUNT(IndepYear) FROM country WHERE IndepYear IS NOT NULL;
    
    Output:
    
    ![image](https://user-images.githubusercontent.com/82821693/116412902-0540e380-a82f-11eb-9d40-ae01b7d7457c.png)



# Sakila

1. List all actors.

   Input:
   
   SELECT first_name, last_name FROM actor;
   
   Output:
   
   ![image](https://user-images.githubusercontent.com/82821693/116413555-a92a8f00-a82f-11eb-8adb-f3067e63199b.png)

2. Find the surname of the actor with the forename 'John'.

   Input:
   
   SELECT last_name FROM actor WHERE first_name = 'John';
   
   Output:
   
   ![image](https://user-images.githubusercontent.com/82821693/116414022-08889f00-a830-11eb-8d78-07585da0fe75.png)
