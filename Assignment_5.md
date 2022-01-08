#### film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en uzun (length) 5 filmi sıralayınız.
select title, length from film 
where title LIKE '%n' 
Order by length desc
limit 5;

#### film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en kısa (length) ikinci(6,7,8,9,10) 5 filmi(6,7,8,9,10) sıralayınız.
select title from film 
where title LIKE '%n' 
Order by length asc
offset 5
limit 5;

#### customer tablosunda bulunan last_name sütununa göre azalan yapılan sıralamada store_id 1 olmak koşuluyla ilk 4 veriyi sıralayınız.
select * from customer
where store_id=1 
ORDER BY last_name desc
limit 4;
