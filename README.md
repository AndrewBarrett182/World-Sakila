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
    
      | Dutch                     |
      | English                   |
      | Papiamento                |
      | Spanish                   |
      | Balochi                   |
      | Dari                      |
      | Pashto                    |
      | Turkmenian                |
      | Uzbek                     |
      | Ambo                      |
      | Chokwe                    |
      | Kongo                     |
      | Luchazi                   |
      | Luimbe-nganguela          |
      | Luvale                    |
      | Mbundu                    |
      | Nyaneka-nkhumbi           |
      | Ovimbundu                 |
      | Albaniana                 |
      | Greek                     |
      | Macedonian                |
      | Catalan                   |
      | French                    |
      | Portuguese                |
      | Arabic                    |
      | Hindi                     |
      | Indian Languages          |
      | Italian                   |
      | Armenian                  |
      | Azerbaijani               |
      | Samoan                    |
      | Tongan                    |
      | Creole English            |
      | Canton Chinese            |
      | German                    |
      | Serbo-Croatian            |
      | Vietnamese                |
      | Czech                     |
      | Hungarian                 |
      | Polish                    |
      | Romanian                  |
      | Slovene                   |
      | Turkish                   |
      | Lezgian                   |
      | Russian                   |
      | Kirundi                   |
      | Swahili                   |
      | Adja                      |
      | Aizo                      |
      | Bariba                    |
      | Fon                       |
      | Ful                       |
      | Joruba                    |
      | Somba                     |
      | Busansi                   |
      | Dagara                    |
      | Dyula                     |
      | Gurma                     |
      | Mossi                     |
      | Bengali                   |
      | Chakma                    |
      | Garo                      |
      | Khasi                     |
      | Marma                     |
      | Santhali                  |
      | Tripuri                   |
      | Bulgariana                |
      | Romani                    |
      | Creole French             |
      | Belorussian               |
      | Ukrainian                 |
      | Garifuna                  |
      | Maya Languages            |
      | Aimará                    |
      | Guaraní                   |
      | Ketšua                    |
      | Japanese                  |
      | Bajan                     |
      | Chinese                   |
      | Malay                     |
      | Malay-English             |
      | Asami                     |
      | Dzongkha                  |
      | Nepali                    |
      | Khoekhoe                  |
      | Ndebele                   |
      | San                       |
      | Shona                     |
      | Tswana                    |
      | Banda                     |
      | Gbaya                     |
      | Mandjia                   |
      | Mbum                      |
      | Ngbaka                    |
      | Sara                      |
      | Eskimo Languages          |
      | Punjabi                   |
      | Romansh                   |
      | Araucan                   |
      | Rapa nui                  |
      | Dong                      |
      | Hui                       |
      | Mantšu                    |
      | Miao                      |
      | Mongolian                 |
      | Puyi                      |
      | Tibetan                   |
      | Tujia                     |
      | Uighur                    |
      | Yi                        |
      | Zhuang                    |
      | Akan                      |
      | Gur                       |
      | Kru                       |
      | Malinke                   |
      | [South]Mande              |
      | Bamileke-bamum            |
      | Duala                     |
      | Fang                      |
      | Maka                      |
      | Mandara                   |
      | Masana                    |
      | Tikar                     |
      | Boa                       |
      | Luba                      |
      | Mongo                     |
      | Ngala and Bangi           |
      | Rundi                     |
      | Rwanda                    |
      | Teke                      |
      | Zande                     |
      | Mbete                     |
      | Mboshi                    |
      | Punu                      |
      | Sango                     |
      | Maori                     |
      | Arawakan                  |
      | Caribbean                 |
      | Chibcha                   |
      | Comorian                  |
      | Comorian-Arabic           |
      | Comorian-French           |
      | Comorian-madagassi        |
      | Comorian-Swahili          |
      | Crioulo                   |
      | Moravian                  |
      | Silesiana                 |
      | Slovak                    |
      | Southern Slavic Languages |
      | Afar                      |
      | Somali                    |
      | Danish                    |
      | Norwegian                 |
      | Swedish                   |
      | Berberi                   |
      | Sinaberberi               |
      | Bilin                     |
      | Hadareb                   |
      | Saho                      |
      | Tigre                     |
      | Tigrinja                  |
      | Basque                    |
      | Galecian                  |
      | Estonian                  |
      | Finnish                   |
      | Amhara                    |
      | Gurage                    |
      | Oromo                     |
      | Sidamo                    |
      | Walaita                   |
      | Saame                     |
      | Fijian                    |
      | Faroese                   |
      | Kosrean                   |
      | Mortlock                  |
      | Pohnpei                   |
      | Trukese                   |
      | Wolea                     |
      | Yap                       |
      | Mpongwe                   |
      | Punu-sira-nzebi           |
      | Gaeli                     |
      | Kymri                     |
      | Abhyasi                   |
      | Georgiana                 |
      | Osseetti                  |
      | Ewe                       |
      | Ga-adangme                |
      | Kissi                     |
      | Kpelle                    |
      | Loma                      |
      | Susu                      |
      | Yalunka                   |
      | Diola                     |
      | Soninke                   |
      | Wolof                     |
      | Balante                   |
      | Mandyako                  |
      | Bubi                      |
      | Greenlandic               |
      | Cakchiquel                |
      | Kekchí                    |
      | Mam                       |
      | Quiché                    |
      | Chamorro                  |
      | Korean                    |
      | Philippene Languages      |
      | Chiu chau                 |
      | Fukien                    |
      | Hakka                     |
      | Miskito                   |
      | Haiti Creole              |
      | Bali                      |
      | Banja                     |
      | Batakki                   |
      | Bugi                      |
      | Javanese                  |
      | Madura                    |
      | Minangkabau               |
      | Sunda                     |
      | Gujarati                  |
      | Kannada                   |
      | Malajalam                 |
      | Marathi                   |
      | Orija                     |
      | Tamil                     |
      | Telugu                    |
      | Urdu                      |
      | Irish                     |
      | Bakhtyari                 |
      | Gilaki                    |
      | Kurdish                   |
      | Luri                      |
      | Mazandarani               |
      | Persian                   |
      | Assyrian                  |
      | Icelandic                 |
      | Hebrew                    |
      | Friuli                    |
      | Sardinian                 |
      | Circassian                |
      | Ainu                      |
      | Kazakh                    |
      | Tatar                     |
      | Gusii                     |
      | Kalenjin                  |
      | Kamba                     |
      | Kikuyu                    |
      | Luhya                     |
      | Luo                       |
      | Masai                     |
      | Meru                      |
      | Nyika                     |
      | Turkana                   |
      | Kirgiz                    |
      | Tadzhik                   |
      | Khmer                     |
      | Tšam                      |
      | Kiribati                  |
      | Tuvalu                    |
      | Lao                       |
      | Lao-Soung                 |
      | Mon-khmer                 |
      | Thai                      |
      | Bassa                     |
      | Gio                       |
      | Grebo                     |
      | Mano                      |
      | Mixed Languages           |
      | Singali                   |
      | Sotho                     |
      | Zulu                      |
      | Lithuanian                |
      | Luxembourgish             |
      | Latvian                   |
      | Mandarin Chinese          |
      | Monegasque                |
      | Gagauzi                   |
      | Malagasy                  |
      | Dhivehi                   |
      | Mixtec                    |
      | Náhuatl                   |
      | Otomí                     |
      | Yucatec                   |
      | Zapotec                   |
      | Marshallese               |
      | Bambara                   |
      | Senufo and Minianka       |
      | Songhai                   |
      | Tamashek                  |
      | Maltese                   |
      | Burmese                   |
      | Chin                      |
      | Kachin                    |
      | Karen                     |
      | Kayah                     |
      | Mon                       |
      | Rakhine                   |
      | Shan                      |
      | Bajad                     |
      | Buryat                    |
      | Dariganga                 |
      | Dorbet                    |
      | Carolinian                |
      | Chuabo                    |
      | Lomwe                     |
      | Makua                     |
      | Marendje                  |
      | Nyanja                    |
      | Ronga                     |
      | Sena                      |
      | Tsonga                    |
      | Tswa                      |
      | Hassaniya                 |
      | Tukulor                   |
      | Zenaga                    |
      | Bhojpuri                  |
      | Chichewa                  |
      | Ngoni                     |
      | Yao                       |
      | Dusun                     |
      | Iban                      |
      | Mahoré                    |
      | Afrikaans                 |
      | Caprivi                   |
      | Herero                    |
      | Kavango                   |
      | Nama                      |
      | Ovambo                    |
      | Malenasian Languages      |
      | Polynesian Languages      |
      | Hausa                     |
      | Kanuri                    |
      | Songhai-zerma             |
      | Bura                      |
      | Edo                       |
      | Ibibio                    |
      | Ibo                       |
      | Ijo                       |
      | Tiv                       |
      | Sumo                      |
      | Niue                      |
      | Fries                     |
      | Maithili                  |
      | Newari                    |
      | Tamang                    |
      | Tharu                     |
      | Nauru                     |
      | Brahui                    |
      | Hindko                    |
      | Saraiki                   |
      | Sindhi                    |
      | Cuna                      |
      | Embera                    |
      | Guaymí                    |
      | Pitcairnese               |
      | Bicol                     |
      | Cebuano                   |
      | Hiligaynon                |
      | Ilocano                   |
      | Maguindanao               |
      | Maranao                   |
      | Pampango                  |
      | Pangasinan                |
      | Pilipino                  |
      | Waray-waray               |
      | Palau                     |
      | Papuan Languages          |
      | Tahitian                  |
      | Avarian                   |
      | Bashkir                   |
      | Chechen                   |
      | Chuvash                   |
      | Mari                      |
      | Mordva                    |
      | Udmur                     |
      | Bari                      |
      | Beja                      |
      | Chilluk                   |
      | Dinka                     |
      | Fur                       |
      | Lotuko                    |
      | Nubian Languages          |
      | Nuer                      |
      | Serer                     |
      | Bullom-sherbro            |
      | Kono-vai                  |
      | Kuranko                   |
      | Limba                     |
      | Mende                     |
      | Temne                     |
      | Nahua                     |
      | Sranantonga               |
      | Czech and Moravian        |
      | Ukrainian and Russian     |
      | Swazi                     |
      | Seselwa                   |
      | Gorane                    |
      | Hadjarai                  |
      | Kanem-bornu               |
      | Mayo-kebbi                |
      | Ouaddai                   |
      | Tandjile                  |
      | Ane                       |
      | Kabyé                     |
      | Kotokoli                  |
      | Moba                      |
      | Naudemba                  |
      | Watyi                     |
      | Kuy                       |
      | Tokelau                   |
      | Arabic-French             |
      | Arabic-French-English     |
      | Ami                       |
      | Atayal                    |
      | Min                       |
      | Paiwan                    |
      | Chaga and Pare            |
      | Gogo                      |
      | Ha                        |
      | Haya                      |
      | Hehet                     |
      | Luguru                    |
      | Makonde                   |
      | Nyakusa                   |
      | Nyamwesi                  |
      | Shambala                  |
      | Acholi                    |
      | Ganda                     |
      | Gisu                      |
      | Kiga                      |
      | Lango                     |
      | Lugbara                   |
      | Nkole                     |
      | Soga                      |
      | Teso                      |
      | Tagalog                   |
      | Karakalpak                |
      | Goajiro                   |
      | Warrau                    |
      | Man                       |
      | Muong                     |
      | Nung                      |
      | Tho                       |
      | Bislama                   |
      | Futuna                    |
      | Wallis                    |
      | Samoan-English            |
      | Soqutri                   |
      | Northsotho                |
      | Southsotho                |
      | Venda                     |
      | Xhosa                     |
      | Bemba                     |
      | Chewa                     |
      | Lozi                      |
      | Nsenga                    |

15. List the names and GNP of the world's top 10 richest countries.

    Input:
    
    SELECT Name, GNP FROM country ORDER BY GNP DESC LIMIT 10;
    
    Output:
    
    ![image](https://user-images.githubusercontent.com/82821693/116398337-9445ff80-a81f-11eb-8663-6a9575f76e0d.png)
