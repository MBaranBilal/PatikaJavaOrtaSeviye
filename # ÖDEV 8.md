## ÖDEV 8

1.**test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.**

```
CREATE TABLE employee(
	id INTEGER,
	name VARCHAR(50),
	birthday DATE,
	email VARCHAR(100)
);
```

2.**Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.**
```
insert into employee (id, name, birthday, email) values (1, 'Cortney', '1993-11-27', 'cculpin0@deviantart.com');
insert into employee (id, name, birthday, email) values (2, 'Hew', '1924-03-22', 'hhartell1@oaic.gov.au');
insert into employee (id, name, birthday, email) values (3, 'Ingelbert', '1986-07-19', 'iarkin2@princeton.edu');
insert into employee (id, name, birthday, email) values (4, 'Loralee', '1952-04-16', 'lwillden3@prnewswire.com');
insert into employee (id, name, birthday, email) values (5, 'Harlin', '1967-01-23', 'hhartington4@sbwire.com');
 ...
 (Kopyala yapıştır işlemi olduğundan tamamını paylaşma gereği duymadım.)
```
3.**Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.**

```
UPDATE employee
SET name='Baran'
WHERE email LIKE'rsw%'
RETURNING *;

UPDATE employee
SET birthday='2000-03-10'
WHERE name LIKE 'B%'
RETURNING *;

UPDATE employee
SET email='patikajava@kodluyoruz.com'
WHERE id BETWEEN 11 AND 15
RETURNING *;

UPDATE employee
SET name='XXXX'
WHERE name LIKE 'D%e' OR id IN(3,18,22)
RETURNING *;

UPDATE employee
SET birthday='2023-08-22'
WHERE email LIKE 'd%a%'
RETURNING *;
```

4.**Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.**

```
DELETE FROM employee
WHERE name='XXXX' AND id=45
RETURNING *;

DELETE FROM employee
WHERE email LIKE 'sw%'
RETURNING *;

DELETE FROM employee
WHERE id=3
RETURNING *;

DELETE FROM employee
WHERE email LIKE '%gov%'
RETURNING *;

DELETE FROM employee
WHERE name LIKE '%k'
RETURNING *;

```
