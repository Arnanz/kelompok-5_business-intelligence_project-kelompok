# Data Warehouse - Kelompok 5

Proyek Business Intelligence untuk implementasi Data Warehouse dengan dataset Northwind Traders yang dibuat oleh Microsoft untuk tujuan edukasi dan demonstrasi. Basis data ini merepresentasikan skenario bisnis perusahaan dagang gourmet fiktif bernama "Northwind Traders" menggunakan Pentaho Data Integration (PDI) dan MySQL.

### Dataset

Struktur datasetnya mencakup informasi dengan atribut:

- Customers: Informasi tentang pelanggan Northwind.
- Employees: Data karyawan dan wilayah penjualan mereka.
- Products: Daftar produk yang dijual, termasuk harga dan kategori.
- Categories: Kategori produk (misalnya, minuman, makanan laut).
- Orders: Detail pesanan yang dilakukan oleh pelanggan.
- Order Details: Item spesifik dalam setiap pesanan.
- Shippers: Informasi tentang perusahaan pengiriman yang digunakan.
- Suppliers: Data pemasok produk.

## Arsitektur Data Warehouse

### Skema Data Warehouse (Star Schema)

Proyek ini menggunakan **Star Schema** yang terdiri dari:

#### Fact Table

- **fact_sales**: (fact_sales_id, product_id, customer_id, employee_id, shipper_id, quantity, unit_price, discount, total_sales, freight, order_date, order_id)

#### Dimension Tables

1. **dim_employee**:  (employee_id, employee_name, title, city, country)
2. **dim_product**: (product_id, product_name, quantity_per_unit, unit_price, discontinued, cetegory)
3. **dim_shipper**: (shipper_id, company_name)
4. **dim_customer**: (customer_id, company_name, contact_name, city, country)