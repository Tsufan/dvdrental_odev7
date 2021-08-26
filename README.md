# dvdrental_odev7
patika.dev dvdrental örnek veri tabanı ile sorgular ödev7

1) film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.
```
SELECT rating, COUNT(*) FROM film
GROUP BY rating;
```
![1](sorgu_1.jpg)
***
2) film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.
```
SELECT replacement_cost, COUNT(*) FROM film
GROUP BY replacement_cost
HAVING COUNT(*) > 50
ORDER BY COUNT(*);
```
![2](sorgu_2.jpg)
***
3) customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir?
```
SELECT store_id, COUNT(*) FROM customer
GROUP BY store_id;
```
![3](sorgu_3.jpg)
***
4)city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıra country_id bilgisini ve şehir sayısını paylaşınız.
```
SELECT country_id, COUNT(*) FROM city
GROUP BY country_id
ORDER BY COUNT(*) DESC
LIMIT 1;
```
![4](sorgu_4.jpg)
