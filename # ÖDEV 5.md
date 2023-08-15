## ÖDEV 5

1.**film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en uzun (length) 5 filmi sıralayınız.**

```
dvdrental=# SELECT title FROM film
dvdrental-# WHERE title LIKE '%n'
dvdrental-# ORDER BY length DESC
dvdrental-# LIMIT 5;
```

2.**film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en kısa (length) ikinci(6,7,8,9,10) 5 filmi(6,7,8,9,10) sıralayınız.**

```
dvdrental=# SELECT title,length FROM film
dvdrental-# WHERE title LIKE '%n'
dvdrental-# ORDER BY length ASC
dvdrental-# OFFSET 5
dvdrental-# LIMIT 5;
```

3.**customer tablosunda bulunan last_name sütununa göre azalan yapılan sıralamada store_id 1 olmak koşuluyla ilk 4 veriyi sıralayınız.**

```
dvdrental=# SELECT last_name,store_id FROM customer
dvdrental-# WHERE store_id=1
dvdrental-# ORDER BY last_name DESC
dvdrental-# LIMIT 4;
```