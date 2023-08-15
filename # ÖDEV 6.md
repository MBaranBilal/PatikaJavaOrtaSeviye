## ÖDEV 6

1.**film tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?**

```
dvdrental=# SELECT ROUND(AVG(rental_rate),3) FROM film;
```

2.**film tablosunda bulunan filmlerden kaç tanesi 'C' karakteri ile başlar?**

```
dvdrental=# SELECT COUNT(*) FROM film
dvdrental-# WHERE title LIKE 'C%';
```

3.**film tablosunda bulunan filmlerden rental_rate değeri 0.99 a eşit olan en uzun (length) film kaç dakikadır?**

```
dvdrental=# SELECT MAX(length) FROM film
dvdrental-# WHERE rental_rate=0.99;
```

4.**film tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?**

```
dvdrental=# SELECT COUNT(DISTINCT replacement_cost) FROM film
dvdrental-# WHERE length>150;
```
