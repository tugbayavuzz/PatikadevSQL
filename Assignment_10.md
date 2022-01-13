Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.



#### city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz LEFT JOIN sorgusunu yazınız.

select city,country from city
left join country on city.city_id = country.country_id;

#### customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz RIGHT JOIN sorgusunu yazınız.

select first_name, last_name from customer
right join payment on customer.customer_id = payment.customer_id; --önce tablo 2 deki veriler alınır.Customer_id ortak sütun


#### customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz FULL JOIN sorgusunu yazınız.
select first_name, last_name from customer
full join rental on customer.customer_id = rental.customer_id;
