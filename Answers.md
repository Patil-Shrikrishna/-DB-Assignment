# -DB-Assignment

A database assignment for the role of Jr. Full Stack Developer at Future Skills.

### Read the diagram carefully and answer the below questions.

![ecommerce table](https://raw.githubusercontent.com/iAmritMalviya/DB-Assignment/main/product-management-ecommerce-table-.webp)

**Questions**

### 1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.

The link between "Product" and "Product_Category" is made using a foreign key. This key in the "Product" table points to the main key in the "Product_Category" table. This connection indicates that each product is linked to a particular category.

In the "Product" table, the "category_id" column acts as a foreign key, referring to the "id" column in the "Product_Category" table.

This relationship forms a link between products and their specific categories. It allows for easy organization and retrieval of information related to product categories when querying the "Product" data. The use of foreign keys ensures data accuracy by confirming that each product's category corresponds to a valid and existing category in the "Product_Category" data.

### 2. How could you ensure that each product in the "Product" table has a valid category assigned to it?

To make sure each product in the "Product" table has the right category, we use a foreign key. Think of it like a rule in the database that checks if the "category_id" in the "Product" table matches the "id" in the "Product_Category" table.

How to include a foreign key constraint:

FOREIGN KEY (category_id) REFERENCES product_category(id)

This rule stops anyone from adding a new product with a "category_id" that doesn't exist in the "Product_Category" table. It's like a safety check to keep the data in good shape. If someone tries to add a product with an invalid category, the database says, "Hey, that category doesn't exist!" This way, we make sure every product has a real and valid category, keeping our data accurate and reliable.
