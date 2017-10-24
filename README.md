-- # SQL-Joins-Peer-Challenge

- [ ] text
- [x] text

-- Answers to questions:
-- 1. 
SELECT * FROM "customers" JOIN "addresses" ON "customers"."id" = "addresses"."id";

-- 2. 
SELECT * FROM "orders" JOIN "line_items" ON "orders"."id" = "line_items"."id";

-- 3.
SELECT “products”.“description” , “warehouse”.“warehouse” FROM “products”
JOIN “warehouse_product” ON “products”.“id” = “warehouse_product”.“product_id” JOIN “warehouse”
ON “warehouse”.“id” = “warehouse_product”.“warehouse_id” WHERE “products”.“description” = ‘cheetos’  ;

--4. 
SELECT “products”.“description” , “warehouse”.“warehouse” FROM “products”
JOIN “warehouse_product” ON “products”.“id” = “warehouse_product”.“product_id” JOIN “warehouse”
ON “warehouse”.“id” = “warehouse_product”.“warehouse_id” WHERE “products”.“description” = ‘diet pepsi’  ;

--6.
SELECT COUNT(*) FROM "customers";

--7. 
SELECT COUNT(*) FROM "products";

--8. 
SELECT SUM("on_hand") FROM "warehouse_product" WHERE "product_id" = 6;
