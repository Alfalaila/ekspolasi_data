# ekspolasi_data
select*from customer c ;
SELECT "Marital Status", AVG(age) AS "Rata-Rata Umur"
FROM customer
GROUP BY "Marital Status";

SELECT gender, AVG(age) AS "Rata-Rata Umur"
FROM customer
GROUP BY gender;

select * from transaksi t ;
select store.storename, sum("transaksi".qty) as "Total Quantity"
from store inner join "transaksi"
on store.storeid = "transaksi".storeid
group by store.storename 
order by "Total Quantity" desc
limit 1;

select product."Product Name", sum("transaksi".totalamount) as "Total Amount"
from product inner join transaksi
on product.productid = "transaksi".productid 
group by product."Product Name" 
order by "Total Amount" desc
limit 1; 
