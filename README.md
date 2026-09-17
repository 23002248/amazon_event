# Amazon Platform - System Test Plan & Manual Test Cases

Comprehensive enterprise-grade Test Plan and Manual Test Case repository for the **Amazon E-Commerce Platform**, developed based on 54 core customer events and platform features.

---

## 📁 Repository Contents

| File Name | Format | Description |
| :--- | :--- | :--- |
| **`Test Plan Document.xlsx`** | Excel Workbook | Complete master workbook containing **`Amazon Testing`** (with dynamic formula KPIs), **`Flipkart Testing`**, and **`Test Plan Template`**. |
| **`Amazon_Platform_Test_Plan.xlsx`** | Excel Workbook | Standalone spreadsheet dedicated exclusively to the **54 Amazon features** with automated execution summary metrics. |
| **`Amazon_Test_Plan_and_Test_Cases.xlsx`** | Excel Workbook | Test Plan & Cases formatted in alignment with the Katalon Manual Test Case Template including metadata & traceability. |
| **`Amazon_Test_Plan_and_Test_Cases.docx`** | Word Document | Formal QA test specification report with executive summary, quality gates, and formatted test tables. |
| **`Amazon_Test_Plan_and_Test_Cases.md`** | Markdown | Complete test plan and 54-case test suite in GitHub Markdown format for quick browsing. |
| **`Untitled spreadsheet.xlsx`** | Excel Workbook | Original source event catalog containing the 54 target Amazon feature requirements. |
| **`WhatsApp Image 2026-09-17 at 10.57.35 AM.jpeg`** | Image | Reference template specification for manual test case structure. |

---

## 📊 QA Execution Summary (Amazon Platform)

The test suite includes active Excel formulas providing real-time visibility into test run status:

| Metric | Formula / Value | Description |
| :--- | :--- | :--- |
| **Total Tests** | `=COUNTA(A14:A67)` (54) | Total test scenarios mapped across all identified modules |
| **Passed** | `=COUNTIF(H14:H67, "Passed")` | Successfully executed test cases meeting expected results |
| **Failed** | `=COUNTIF(H14:H67, "Failed")` | Defects or anomalies identified during execution |
| **Blocked** | `=COUNTIF(H14:H67, "Blocked")` | Tests obstructed by prerequisite environment blockers |
| **Not Executed** | `=COUNTIF(H14:H67, "Not Executed")` | Remaining tests pending execution in current test cycle |
| **Execution Progress** | `=IF(COUNTA=0, 0, COUNTIF("<>Not Executed")/COUNTA)` | Percentage of total test suite executed |
| **Pass Rate** | `=IFERROR(Passed / (Passed + Failed), 0)` | Overall test pass yield |
| **Status** | `=IF(H4=1, "Completed", IF(H4>0, "In Progress", "Not Started"))` | High-level test cycle milestone status |

---

## 🎯 Test Scope & Feature Modules (54 Scenarios)

The test cases cover all core user journeys across the Amazon platform:

1. **User Authentication & Security:** Sign In (`TC001`), Secure Sign Out (`TC023`), New User 'Start here' Registration (`TC033`).
2. **Product Discovery & Search:** Keyword Search with Auto-suggest (`TC002`), All Category Scope Filter (`TC026`), Multi-facet Filters (`TC053`), Zero-results Typo Correction (`TC054`), Sorting Bar (`TC017`).
3. **Shopping Cart Management:** Add to Cart from PDP (`TC003`, `TC051`), Update Quantity & Subtotal (`TC050`), Remove / Save for Later (`TC052`).
4. **Checkout & Payment:** Secure Checkout Initiation (`TC004`), Multi-rail Payment Gateway (`TC005`, `TC047`), Stored Payment Methods & Wallet (`TC048`), Order Confirmation (`TC049`).
5. **Address & Delivery:** Address Book & Contact (`TC006`), Header Pincode Picker (`TC025`), PDP Pincode SLA Availability (`TC046`), Change Shipping Address in Checkout (`TC045`), Country / Currency Switcher (`TC009`).
6. **Order Management & Returns:** Order History & Invoices (`TC007`), Return / Replacement Flow (`TC014`), Online Return Centre (`TC027`).
7. **User Account & Profile:** Profile Updates (`TC008`), 'Your Account' Dashboard (`TC015`), Wishlist (`TC016`), Browsing History (`TC037`).
8. **Customer Service & Support:** Chatbot Support (`TC022`), 'Call Me Now' Telephony Support (`TC044`), Help Portal Articles (`TC028`).
9. **Prime & Exclusive Programs:** Prime Membership Management (`TC034`), Prime Exclusive Perks (`TC043`), Today's Deals & Lightning Deals (`TC024`), Coupons & Cashback (`TC019`).
10. **Ecosystem & Auxiliary Services:** Amazon Showroom 3D (`TC036`), Seller Central (`TC012`, `TC035`), Digital Content & Kindle Cloud Reader (`TC040`, `TC041`), Hardware Devices (`TC039`), Appstore (`TC038`), AWS (`TC029`), IMDb (`TC030`), Amazon Music (`TC031`), Logo Redirection (`TC032`), Product Customization (`TC018`), Legal Terms & Privacy (`TC020`, `TC041`, `TC042`), Recommendations (`TC021`), Social Links (`TC010`).

---

## 📋 Test Case Table Schema

Each test scenario follows the standardized 8-column enterprise QA structure:

```
[Test Case ID] | [Module] | [Test Scenario] | [Test Steps] | [Test Data] | [Expected Result] | [Actual Result] | [Status]
```

### Example Test Case Entry
* **Test Case ID:** `TC001`
* **Module:** `Authentication`
* **Test Scenario:** `Verify user authentication with valid credentials`
* **Test Steps:** `Open Amazon → Click Account & Lists → Enter registered email → Click Continue → Enter valid password → Click Sign In`
* **Test Data:** `Valid email & password`
* **Expected Result:** `User should be successfully logged in and redirected to homepage with personalized greeting 'Hello, [Name]'`
* **Actual Result:** `Done as expected`
* **Status:** `Passed`