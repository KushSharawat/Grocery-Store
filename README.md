# Grocery Store: Online Shopping Website

A full-stack e-commerce web application for an online grocery store, built with **ASP.NET Web Forms (C#)** and **SQL Server**. Customers can register, browse products by category, search, add items to a cart, place orders and view their order history.

## Features

- **User accounts:** registration and login, with a check for duplicate email addresses
- **Product catalogue:** all products, plus Fruits and Vegetables category pages (loaded from the database)
- **Search:** find products by name
- **Shopping cart:** add products, adjust quantities and see a running total
- **Checkout:** delivery address form, with an order saved under a unique order code
- **Order history and details:** past orders with status, and the line items for each order
- **Contact and About pages:** contact form submissions are stored in a Feedback table
- **Shared layout:** a master page (`GrocerySite.master`) for a consistent header, navigation and footer

## Tech stack

| Layer | Technology |
|---|---|
| Front end | ASP.NET Web Forms (`.aspx`), HTML, CSS |
| Back end | C# code-behind (`.aspx.cs`), ADO.NET (`SqlConnection`, `SqlCommand`) |
| Database | Microsoft SQL Server (Express) |

## Database tables

`Registration`, `Login`, `CategoryMaster`, `Product`, `Order`, `OrderedProducts`, `Feedback`

## How to run

1. Install **Visual Studio** (with the *ASP.NET and web development* workload) and **SQL Server Express**.
2. Create a database called `GROCERYDB` containing the tables above.
3. The connection string in `Web.config` points to the local default instance:
   ```xml
   Data Source=.\SQLEXPRESS;Initial Catalog=GROCERYDB;Integrated Security=True
   ```
   Change it if your SQL Server instance has a different name.
4. Open the folder in Visual Studio (**File → Open → Web Site**) and press **F5**.

## What I'd improve next

- Switch all queries to **parameterised SQL** (`SqlParameter`) to prevent SQL injection
- Hash passwords instead of storing them as plain text
- Add the database creation script to the repo
