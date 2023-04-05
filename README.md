# SQL-Odev4

1. **film** tablosunda bulunan replacement_cost sütununda bulunan birbirinden farklı değerleri sıralayınız.
```sql
SELECT DISTINCT replacement_cost FROM film 
```
2. **film** tablosunda bulunan replacement_cost sütununda birbirinden farklı kaç tane veri vardır?
```sql
SELECT COUNT(distinct replacement_cost) FROM film 
```
3. **film** tablosunda bulunan film isimlerinde (title) kaç tanesini T karakteri ile başlar ve aynı zamanda rating 'G' ye eşittir?
```sql
SELECT COUNT (distinct title ) FROM film WHERE title ~~* 't%' AND rating = 'G'
```
4. **country** tablosunda bulunan ülke isimlerinden (country) kaç tanesi 5 karakterden oluşmaktadır?
```sql
SELECT COUNT(distinct country) FROM country WHERE country ~~ '_____'
SELECT COUNT(distinct country) FROM country WHERE country like '_____'
```
5. **city** tablosundaki şehir isimlerinin kaç tanesi 'R' veya r karakteri ile biter?
```sql
SELECT COUNT(distinct city) FROM city WHERE city ILIKE '%r'
SELECT COUNT(distinct city) FROM city WHERE city ~~* '%r'
```
