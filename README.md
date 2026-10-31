# Online Shop / Sklep internetowy

## EN

### Overview

Online Shop is a database project written in Oracle SQL, developed as a second-year university project at Kielce University of Technology.
The project presents a simplified database model of an online shopping platform inspired by services such as Allegro, eBay, and Amazon. Its purpose is to represent the main elements of an e-commerce system, including users, products, categories, sellers, buyers, shopping carts, deliveries, payments, invoices, and addresses.
The database structure is based on entities and relationships that describe how the individual elements of an online shop are connected. It includes one-to-many and many-to-many relationships, as well as inheritance between users, sellers, and buyers.

### Database Entities

1. Shop
2. Category
3. Manufacturer
4. Delivery
5. User
6. Product
7. Seller
8. Buyer
9. Address
10. Shopping Cart
11. Invoice
12. Payment
13. Cart_Product (junction entity)
14. Category_Manufacturer (junction entity)

### Relationships

**One-to-many relationships:**

- Address → User – one address can be assigned to multiple users.
- Address → Delivery – one address can be associated with multiple deliveries.
- Shop → Shopping Cart – one shop can contain multiple shopping carts.
- Delivery → Shopping Cart – one delivery method can be associated with multiple shopping carts.
- Buyer → Shopping Cart – one buyer can have multiple shopping carts.
- Shopping Cart → Invoice – one shopping cart can be associated with multiple invoices.
- Payment → Invoice – one payment can be associated with multiple invoices.
- Category → Product – one category can contain multiple products.
- Seller → Product – one seller can offer multiple products.

**Many-to-many relationships:**

- Shopping Cart ↔ Product (through the `Cart_Product` entity).
  - One shopping cart can contain multiple products.
  - One product can be included in multiple shopping carts.
- Category ↔ Manufacturer ↔ Product (through the `Category_Manufacturer` entity).
  - Multiple categories and manufacturers can be associated with multiple products.

**Inheritance relationships:**

- User → Seller – Seller inherits from User.
- User → Buyer – Buyer inherits from User.

### Diagram

![Diagram](screenshots/diagram.png)

### Technologies

- Oracle SQL
- Oracle Database

---

## PL

### Opis

Online Shop to projekt bazy danych napisany w języku Oracle SQL, zrealizowany na drugim roku studiów na Politechnice Świętokrzyskiej.
Projekt przedstawia uproszczony model bazy danych sklepu internetowego, inspirowany serwisami takimi jak Allegro, eBay czy Amazon. Jego celem jest odwzorowanie najważniejszych elementów systemu e-commerce, takich jak użytkownicy, towary, kategorie, sprzedający, kupujący, koszyki, dostawy, płatności, faktury oraz adresy.
Struktura bazy danych opiera się na encjach i relacjach opisujących powiązania pomiędzy poszczególnymi elementami sklepu internetowego. Uwzględnia relacje jeden do wielu, wiele do wielu, a także dziedziczenie pomiędzy użytkownikiem, sprzedającym i kupującym.

### Encje występujące w bazie danych

1. Sklep
2. Kategoria
3. Producent
4. Dostawa
5. Użytkownik
6. Towar
7. Sprzedający
8. Kupujący
9. Adres
10. Koszyk
11. Faktura
12. Płatność
13. Towar_koszyk (encja pośrednicząca)
14. Kategoria_producent (encja pośrednicząca)

### Relacje między encjami

**Relacje jeden do wielu:**

- Adres → Użytkownik – jeden adres może być przypisany do wielu użytkowników.
- Adres → Dostawa – jeden adres może być powiązany z wieloma dostawami.
- Sklep → Koszyk – w jednym sklepie może znajdować się wiele koszyków.
- Dostawa → Koszyk – jedna dostawa może być powiązana z wieloma koszykami.
- Kupujący → Koszyk – jeden kupujący może posiadać wiele koszyków.
- Koszyk → Faktura – jeden koszyk może być powiązany z wieloma fakturami.
- Płatność → Faktura – jedna płatność może być powiązana z wieloma fakturami.
- Kategoria → Towar – w jednej kategorii może znajdować się wiele towarów.
- Sprzedający → Towar – jeden sprzedający może wystawiać wiele towarów.

**Relacje wiele do wielu:**

- Koszyk ↔ Towar (za pośrednictwem encji `Towar_koszyk`).
  - Jeden koszyk może zawierać wiele towarów.
  - Jeden towar może znajdować się w wielu koszykach.
- Kategoria ↔ Producent ↔ Towar (za pośrednictwem encji `Kategoria_producent`).
  - Wiele kategorii i producentów może być powiązanych z wieloma towarami.

**Relacje nadklasa – podklasa:**

- Użytkownik → Sprzedający – sprzedający dziedziczy po użytkowniku.
- Użytkownik → Kupujący – kupujący dziedziczy po użytkowniku.

### Diagram

![Diagram](screenshots/diagram.png)

### Technologie

- Oracle SQL
- Oracle Database