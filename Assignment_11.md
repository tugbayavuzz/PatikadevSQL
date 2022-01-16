film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?
SELECT COUNT(*) as filmSayısı FROM film WHERE length > (SELECT ROUND(AVG(length)) FROM film);

film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?
SELECT COUNT(*) as filmSayısi FROM film WHERE rental_rate = (SELECT MAX(rental_rate) FROM film); 

film tablosunda en düşük rental_rate ve en düşün replacement_cost değerlerine sahip filmleri sıralayınız.
SELECT title  from film where rental_rate= (SELECT MIN(rental_rate) from film)
AND replacement_cost = (SELECT MIN(replacement_cost) from film);

payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.
SELECT customer_id, SUM(amount) from payment Group by customer_id order by SUM(amount) desc;
