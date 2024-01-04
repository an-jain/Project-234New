select customers.last_name, customers.phone, company_products.name, suppliers.contact_name
from customers join company_orders
on customers.id = company_orders.customer_id
join order_items.order_id
join company_products
on order_items.product_id = company_products.id
join suppliers
on company_products.supplier_id = suppliers.id
