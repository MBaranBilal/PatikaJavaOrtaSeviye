## ÖDEV 7

1.**film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.**

```
dvdrental=# SELECT rating FROM film
dvdrental-# GROUP BY rating;
```

2.**film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.**

```
dvdrental=# SELECT replacement_cost,COUNT(*) FROM film
dvdrental-# GROUP BY replacement_cost
dvdrental-# HAVING COUNT(*)>50;
```

3.**customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir?**

```
dvdrental=# SELECT store_id,COUNT(*) FROM customer
dvdrental-# GROUP BY store_id;
```

4.**city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.**

```
dvdrental=# SELECT country_id,COUNT(*) FROM city
dvdrental-# GROUP BY country_id
dvdrental-# ORDER BY COUNT(*) DESC
dvdrental-# LIMIT 1;
```


