# Caffinity: Online Cafe Management System

CSC 3215 Web Technologies project, Group 07, Section Q (Fall 26-27), American International University-Bangladesh.

Caffinity is a web-based system for running a single cafe. Customers order online (delivery, pickup or QR dine-in) and book tables, kitchen staff manage a live order board, delivery riders update their deliveries, and the cafe owner manages the menu, staff, coupons, settings and sales reports.

> **Current stage: front-end prototype.** All pages are built with HTML, CSS and JavaScript. Data is saved in the browser with `localStorage`, so the full flow works without a server. The next stage replaces `js/data.js` with PHP and MySQL, as described in the project proposal.

## How to run

1. Open the `caffinity` folder in VS Code.
2. Install the **Live Server** extension (by Ritwick Dey).
3. Right-click `index.html` and choose **Open with Live Server**.

You can also double-click `index.html` to open it directly in a browser.

## Demo accounts

| Role | Email | Password |
| --- | --- | --- |
| Customer | customer@caffinity.com | customer123 |
| Kitchen Staff | kitchen@caffinity.com | kitchen123 |
| Delivery Rider | rider@caffinity.com | rider123 |
| Cafe Owner (Admin) | admin@caffinity.com | admin123 |

The login page also has buttons that fill these in for you. To start fresh, log in as the owner and use **Cafe settings > Reset demo data**.

## Try the full order flow

1. Log in as the **customer**, add items from the menu, apply coupon `CAFF10` in the cart and place a delivery order.
2. Log in as **kitchen staff**, start preparing the order and mark it ready.
3. Log in as the **owner**, open **Orders** and assign a rider.
4. Log in as the **rider**, mark the order picked up, out for delivery and delivered (confirm the cash).
5. Log back in as the **customer** to see the order delivered and rate it.

For QR dine-in, open `menu.html?table=4`. Each table's QR code would point to this link with its own table number.

Tip: open two browser windows side by side (for example customer and kitchen). Pages refresh their data every 5 seconds, so changes appear automatically.

## Pages

| Folder | Page | Purpose |
| --- | --- | --- |
| / | `index.html` | Home page with opening status and popular items |
| / | `menu.html` | Browse by category, search, add to cart, QR table banner |
| / | `cart.html` | Change quantities, apply coupon |
| / | `checkout.html` | Delivery, pickup or dine-in details and payment method |
| / | `track-order.html` | Live order status timeline |
| / | `reservation.html` | Request a table |
| / | `login.html`, `register.html`, `forgot-password.html` | Authentication |
| / | `profile.html` | Edit profile and photo, change password, delete account (customers) |
| customer/ | `dashboard.html` | Active orders, order history, reviews, reservations |
| kitchen/ | `dashboard.html` | Live order board: New, Preparing, Ready |
| kitchen/ | `availability.html` | Mark items sold out or available |
| rider/ | `dashboard.html` | Assigned deliveries and status updates |
| rider/ | `history.html` | Completed deliveries and daily totals |
| admin/ | `dashboard.html` | Today's summary, 7-day sales chart, best sellers |
| admin/ | `orders.html` | All orders, assign riders, cancel |
| admin/ | `menu.html` | Menu items and categories |
| admin/ | `reservations.html` | Approve or decline reservations |
| admin/ | `staff.html` | Create, edit, activate or deactivate staff |
| admin/ | `coupons.html` | Coupon codes and offers |
| admin/ | `settings.html` | Opening hours, delivery areas and charges |
| admin/ | `reports.html` | Daily and monthly sales, best sellers, busiest hours |

## Folder structure

```
caffinity/
├── index.html, menu.html, cart.html, checkout.html, ...
├── customer/   kitchen/   rider/   admin/
├── css/style.css     shared styles for every page
└── js/
    ├── data.js       sample data and localStorage helpers
    └── main.js       shared functions (login, cart, validation, toasts)
```

## Technologies

HTML, CSS and JavaScript (front end). Planned: PHP (server side) and MySQL (database).

## Team

| Student ID | Name | Role |
| --- | --- | --- |
| 23-50801-1 | Rifat Ahmed Bhuiyan | Group Leader |
| 23-50935-1 | Fatema Akhter | Member |
| 23-53114-3 | Imamul Islam Shihab | Member |
| 23-54668-3 | Nourin Khan Zerin | Member |
