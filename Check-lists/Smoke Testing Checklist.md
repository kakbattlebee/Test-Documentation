# 📋 Smoke Testing Checklist 🔥
*(Critical post-release checks covering key functionality: checkout, search, pricing, and authentication.)*

## 1️⃣ Authentication & Authorization 🔐
✅ Verify login with valid credentials (email/password)  
❌ Verify login through social media (Google, Facebook, Apple ID, if applicable)  
✅ Verify login failure with incorrect credentials  
✅ Verify password recovery (email dispatch, correct reset link)  
✅ Verify logout functionality and session termination  
✅ Verify access to the user profile after successful login  

## 2️⃣ Ticket Search 🎟️
✅ Verify ticket search using key parameters (date, route, passenger count)  
✅ Verify correct display of search results  
✅ Verify filtering functionality (by price, departure time, transfer availability, etc.)  
✅ Verify sorting functionality (by price, time, route duration)  
✅ Verify appropriate messaging when no results are found  

## 3️⃣ Fare Loading 💰
✅ Verify fares are displayed after selecting a route  
❌ Verify correct pricing information  
❌ Verify included services (baggage, meals, refunds) are displayed correctly  
✅ Verify availability of different fare classes (economy, business, premium)  
✅ Verify real-time fare updates based on demand  

## 4️⃣ Checkout & Payment 💳
✅ Verify the total cost is displayed before payment  
✅ Verify all available payment methods (card, PayPal, Apple Pay, etc.) are functional  
✅ Verify successful ticket purchase  
❌ Verify error handling for failed transactions  
✅ Verify ticket is sent via email/SMS after a successful purchase  
✅ Verify proper redirection for logged-in and guest users  
✅ Verify invoice download availability  

## 5️⃣ General Checks 🛠️
✅ Verify compatibility with different browsers (Chrome, Firefox, Safari, Edge)  
✅ Verify correct UI display on mobile and tablet devices  
✅ Verify security measures (data transfer over HTTPS, protection against SQL injection)  
✅ Verify system stability under high load (search, checkout, authentication)  

---

### 📂 How to Use This Checklist?
- This checklist is designed for **smoke testing** to ensure critical functionalities work after deployment.  
- Tests can be executed **manually or automated**, depending on project requirements.  
- Use **✅ for passed tests**, **❌ for failed tests**, and **🔄 for in-progress tests**.