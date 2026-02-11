🛒 SambalPay Secure Checkout – API Transaction Flow Validation

 📌 Overview

This repository contains the API validation artifacts for the Secure Checkout flow as part of the SambalPay Technical Product Manager assessment.

The objective was to simulate an authenticated user journey involving:

 Secure login using JWT authentication
 Product inventory lookup
 Cart creation and modification
 Token payload inspection for backend user identification

🔄 Transaction Lifecycle Covered

1. Authentication

    Endpoint: `POST /auth/login`
    Retrieves JWT token for secure session handling

2. Inventory Lookup

    Endpoint: `GET /products`
    Identified high-value product and extracted product ID

3. Cart Creation

    Endpoint: `POST /carts`
    Added selected product to user cart

4. Cart Update

    Endpoint: `PUT /carts/{id}`
    Modified product quantity from 1 to 3

5. JWT Analysis

    Decoded token payload to validate `sub` (subject) user mapping

---

 📁 Repository Structure

```
.
├── SambalPay_Checkout_Flow.postman_collection.json
├── data-log.md
├── step4_update_response.png
└── README.md
```

---

 📊 Key Outputs

| Field               | Value |
| ------------------- | ----- |
| Product ID          | 9     |
| JWT Subject (`sub`) | 2     |
| Updated Quantity    | 3     |

---

 🧠 Technical Highlights

 RESTful transaction handling
 Token-based session authentication
 JSON response parsing for relational mapping
 Real-world checkout lifecycle simulation

---
✅ Tools Used

Postman / Bruno for API execution
jwt.io for token decoding

📬 Notes

All requests are organized in the `SambalPay_Checkout_Flow` collection and can be replayed in sequence to reproduce the full transaction lifecycle.


