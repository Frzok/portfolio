# 📝 Test Assignment Solution

## 1. Databases — Quiz

**Answers to the test questions:**

1. `1, 3`  
2. `4`  
3. `2, 4`  
4. `2`  
5. `4`  
6. `2, 4, 5`  
7. `3`  
8. `1`  
9. `2, 3`  
10. `3`

---

## 2. Databases — ER Diagram (Verbal Description)

There are orders (`orders`) which include name, price, town, and customer ID.  
A single order can contain multiple items, and one item can appear in multiple orders — a many-to-many relationship.  
To model this, we create a junction table `Order_Items`.

**Table structure:**

- **Orders:**  
  `id (PK), name, town, price, customer_id (FK)`
- **Items:**  
  `id (PK), name, price`
- **Customers:**  
  `id (PK), full_name, email, phone`
- **Towns:**  
  `id (PK), name`
- **Order_Items (junction table):**  
  `order_id (FK), item_id (FK), quantity`

---

## 3. Integrations (Amazon)

### 🔹 Scenario:

1. A user opens the Amazon storefront and sees a list of products  
2. Clicks on a product to open the product details page  
3. Clicks "Add to Cart"

---

### 📦 REST API

#### ✅ Get Product List

`GET /api/products`

**Response:**
```json
[
  {
    "id": "B00X4WHP5E",
    "name": "Echo Dot (5th Gen)",
    "price": 59.99,
    "short_description": "Smart speaker with Alexa"
  }
]
````

#### ✅ Get Product Details

`GET /api/products/B00X4WHP5E`

**Response:**

```json
{
  "id": "B00X4WHP5E",
  "name": "Echo Dot (5th Gen)",
  "description": "Voice control, smart home integration, and music",
  "price": 59.99,
  "images": ["img1.jpg", "img2.jpg"]
}
```

#### ✅ Add to Cart

`POST /api/cart`

**Request body:**

```json
{
  "product_id": "B00X4WHP5E",
  "quantity": 1
}
```

**Response:**

```json
{
  "message": "Product added to cart",
  "cart_total": 59.99
}
```

---

### 🔄 Sequence Diagram

**Participants:**
`User → Amazon Frontend → API → Database`

**Flow:**

1. `GET /api/products` — load storefront
2. `GET /api/products/{id}` — view product details
3. `POST /api/cart` — add item to cart

---

## 4. Algorithmic Thinking (Sparkasse)

### 📲 Scenario: Top up €100 via the Sparkasse mobile app

1. Turn on the phone
2. Open the Sparkasse app
3. Authenticate (Face ID)
4. Go to the "Handy aufladen" (Top-Up) section
5. Enter mobile phone number
6. Select the amount: **€100**
7. Confirm the payment (pushTAN)
8. Receive a success notification


