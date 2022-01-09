#### film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.
select rating  from film 
GROUP BY rating;

#### film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.

select replacement_cost, COUNT(*) from film 
GROUP BY replacement_cost
HAVING COUNT(*) >50;

#### customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir?
select store_id,customer_id from customer 
group by customer_id, store_id;


#### city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra  en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.
select country_id,COUNT(city) from city
group by country_id
order by COUNT(city) desc 
LIMIT 1
