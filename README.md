# Express TS Starter

Simple express TS starter!

## How to use?

```
$ npm install
$ npm run dev # run development!
```
## Postman Test Collection
You can import the postman collection by download CH5_Postman_Collection file

## Scripts

```
$ npm run build # build typescript project
$ npm start # run in development mode
```
# Database Structure (using dbdiagram.io)
## copy this code to dbdiagram.io

// Use DBML to define your database structure
// Docs: https://dbml.dbdiagram.io/docs

Table users {
  id integer
  user_type string
  email integer
  password timestamp 
}

Table cars {
  id integer
  name string
  type string
  rent_cost integer
  image string
  is_available boolean
  available_at date
}

Table order {
  id integer
  user_email integer
  car_id integer
  start_rent date
  finish_rent date
  rent_status string // 'Pending', 'Rented', 'Returned', 'Cancelled', 'Overdue'
  payment_status boolean
}

Ref: order.user_email > users.email // many-to-one
Ref: order.car_id > cars.id // one-to-many
