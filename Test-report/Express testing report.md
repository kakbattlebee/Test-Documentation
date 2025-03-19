**Test Report: Results of Express Functional and Layout Testing for BeeMarket Website**

---

### **General Information:**

* **Testing Objective:** Conduct rapid testing of core functionalities and layout across main browsers and resolutions for desktop and mobile devices.
* **Start Date:** 12.11.2024
* **End Date:** 16.11.2024
* **Environment:**
  * **Website:**
  * **Browsers:** Chrome, Firefox, Safari, Edge (desktop and mobile)
  * **Resolutions:**
    * Desktop: 1920x1080, 1366x768
    * Mobile: 375x667 (iOS), 360x640 (standard Android)

### **Summary:**

Testing identified several critical, medium, and low-priority issues affecting website functionality and layout. Key functional areas such as authorization, search, filters, adding products to cart and favorites, order placement, and catalog display are operational, but specific key issues require attention to enhance user experience.

### **Main Identified Issues:**

| ID | Issue Description | Status | Priority |
| ----- | ----- | ----- | ----- |
| FUNC-001 | Authorization confirmation code not received by Uzmobile and Mobiuz numbers | Open | High |
| FUNC-002 | Empty order page when accessing from order history after completion | Open | High |
| FUNC-004 | Unauthorized access to other users' personal order data via URL | Open | Critical |
| FUNC-009 | Favorites and comparison reset after page refresh for unauthorized users | Open | High |
| FUNC-014 | Catalog view toggle buttons not functional on mobile | Open | Medium |
| UI-02 | Incorrect alignment of product specifications on comparison page | Open | Medium |
| UI-04 | Partial display of total amount and payable amount on the order page for certain payment types | Open | Medium |

### **Detailed Testing Description by Main Areas:**

#### **1. Functional Testing:**

* **Authorization:** Issues identified with receiving confirmation codes from specific carriers (Uzmobile and Mobiuz), hindering authorization.
* **Product and Category Search:** Core functionality operating correctly, no issues found.
* **Product Filters and Sorting:** Sorting by discount incorrectly places non-discounted products first.
* **Favorites and Cart:** Favorites reset after page refresh for unauthorized users.
* **Order Placement:** Accessing orders from history results in an empty page with console errors.
* **Buttons and Links (Homepage and Category Pages):** Fifth banner 'Buy' button inactive and part of the image, causing user confusion.
* **Product Comparison:** Issues displaying product specifications, especially with more than two products on mobile devices.

#### **2. Layout Testing:**

* **Responsive Design:** Issues identified with button and specification display on mobile devices.
* **Cross-browser Check:** Minor problems like missing animations and incorrect element behavior impacting user experience.

#### **3. Cross-browser Testing:**

* **Chrome, Firefox, Safari, Edge:** Functionalities mostly stable; layout issues with buttons and elements noticed on mobile versions.
* **Mobile Devices:** Catalog view toggle buttons and absence of horizontal scroll for product specifications on the comparison page identified as main issues.

### **Overall Testing Status:**

Out of 21 bugs identified:

* **Critical:** 1 (unauthorized data access via URL)
* **High Priority:** 3 (confirmation code issue, empty order page, favorites reset)
* **Medium Priority:** 8 (non-functional catalog view buttons, comparison page specification issues, alignment issues, etc.)
* **Low Priority:** Remaining bugs, including minor layout and animation problems

