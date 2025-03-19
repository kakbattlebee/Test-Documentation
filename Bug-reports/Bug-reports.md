## 🐞 Bug Report: Incorrect Product Deduction - SIM Card Deducted Instead of Smartphone

### 📝 Description
When attempting to deduct a smartphone from the inventory system, a SIM card was incorrectly deducted instead. The smartphone count did not revert to its original value.

### 🔄 Steps to Reproduce
1. Access the ERP system.
2. Select a smartphone for deduction.
3. Confirm the deduction.
4. After some time, check the remaining stock in the system.

### ❌ Actual Result
- A SIM card was deducted instead of the selected smartphone.
- The smartphone count remained unchanged.

### ✅ Expected Result
- Correct deduction of the selected smartphone.
- No unintended item (SIM card) should be deducted.

### 📌 Additional Information
- Order number: [REDACTED]
- IMEI of the smartphone replaced by a SIM card: [REDACTED]
- Estimated Fix Time: 1 hour
- Priority: 🔥 **Highest**

---

## 🐞 Bug Report: Incorrect Final Price Display After Applying New Year Promo Code (5% Discount)

### 📝 Description
After applying the New Year promo code (5% discount) in the cart and on the checkout page, the final price displayed is incorrect. It shows the discount amount as the total payable amount instead of the correct final price.

### 🔄 Steps to Reproduce
1. Apply the New Year promo code (5%) on the cart page.
2. Check the displayed final price.
3. Apply the promo code on the checkout page.
4. Check the displayed final price again.

### ❌ Actual Result
- The "To Pay" section incorrectly displays the discount amount instead of the final payable price.

### ✅ Expected Result
- Correct final price: Original price minus the 5% discount.

### 📌 Additional Information
- Issue occurs on both cart and checkout pages.

---

## 🐞 Bug Report: API Security Flaw - Unauthorized Data Access

### 📝 Description
The API allows unauthorized users to access sensitive user data by modifying the request payload.

### 🔄 Steps to Reproduce
1. Send a GET request to `/user/details/{user_id}` using an API testing tool (e.g., Postman).
2. Modify `user_id` to another user's ID.
3. Observe the response.

### ❌ Actual Result
- API returns private user details (name, email, phone) without authentication.

### ✅ Expected Result
- API should validate user sessions before returning private data.
- Unauthorized requests should return a `403 Forbidden` response.

### 📌 Additional Information
- Endpoint affected: `/user/details/{user_id}`
- Priority: 🔥 **Critical**

---

## 🐞 Bug Report: API Rate Limiting Not Implemented

### 📝 Description
API lacks rate limiting, allowing unlimited requests in a short period, posing a DDoS risk.

### 🔄 Steps to Reproduce
1. Send 1000+ requests per second to `/search/flights` using a script.
2. Observe API response times and headers.

### ❌ Actual Result
- API accepts unlimited requests without triggering `429 Too Many Requests`.

### ✅ Expected Result
- Implement rate limiting (e.g., 100 requests/minute).
- Exceeded requests should return `429 Too Many Requests`.

### 📌 Additional Information
- Endpoint affected: `/search/flights`
- Priority: ⚠️ **Major**

---

## 🐞 Bug Report: Missing Frontend Validation in Search Fields

### 📝 Description
The search form lacks validation, allowing empty, incorrect inputs, and auto-assigning the date `2025-01-01` without user confirmation if the departure date is missing.

### 🔄 Steps to Reproduce
1. Open the flight search page.
2. Submit empty search fields.
3. Enter invalid city names (e.g., `12345`, `###`, `qwerty`).
4. Enter correct "From" and "To" fields, leave departure date empty, and click "Search".

### ❌ Actual Result
- Empty or invalid data submission is allowed.
- Invalid city names are accepted.
- Departure date defaults to `2025-01-01`.

### ✅ Expected Result
- Frontend validation should prevent submission of empty fields.
- City fields must validate actual city selection from autocomplete.
- Missing departure dates should trigger error prompts rather than assigning default dates.

### 🔥 Priority
- **High** (Disrupts search functionality and negatively affects user experience).

### 📎 UI Design Reference
- Desktop State for Invalid Inputs: [Figma Design](#)
- Mobile State for Invalid Inputs: [Figma Design](#)

