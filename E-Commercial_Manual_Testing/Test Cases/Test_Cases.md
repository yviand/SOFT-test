# TEST CASES

| TC_ID | Req_ID | Title | Precondition | Steps | Expected Result | Priority | Type |
|-------|--------|-------|-------------|-------|----------------|----------|------|
| TC_AUTH_001 | R1 | Register with valid email | User not registered | 1. Go to /register <br> 2. Enter valid email & password <br> 3. Click Register | Account created successfully | High | Positive |
| TC_AUTH_002 | R1 | Register with existing email | Email already exists | 1. Enter duplicated email <br> 2. Submit | Show error: Email already exists | Medium | Negative |
| TC_AUTH_003 | R2 | Email missing "@" symbol | None | Enter `usergmail.com` | Show invalid email format error | High | Negative |
| TC_AUTH_004 | R2 | Email missing domain | None | Enter `user@` | Show invalid email format error | High | Negative |
| TC_AUTH_005 | R2 | XSS injection in email field | None | Enter `<script>alert(1)</script>` | Input is sanitized or blocked | High | Security |
| TC_AUTH_006 | R3 | Password exactly 8 chars | None | Enter `12345678` | Registration successful | High | Boundary |
| TC_AUTH_007 | R3 | Password less than 8 chars | None | Enter `1234567` | Show min length error | High | Boundary |
| TC_AUTH_008 | R3 | Empty password | None | Leave password blank | Show required field error | High | Negative |
| TC_AUTH_009 | R4 | Login with valid credentials | Account exists | Enter correct email & password | Login successful | Critical | Positive |
| TC_AUTH_010 | R4 | Session persists after refresh | Logged in | Refresh page | User remains logged in | Medium | Positive |
| TC_AUTH_011 | R5 | Login with wrong password | Account exists | Enter incorrect password | Show invalid password error | High | Negative |
| TC_AUTH_012 | R5 | Multiple failed login attempts | Account exists | Enter wrong password 5 times | Account temporarily locked | Medium | Security |
| TC_AUTH_013 | R6 | Forgot password with valid email | Account exists | Enter registered email | Reset email sent | High | Positive |
| TC_AUTH_014 | R6 | Forgot password with unregistered email | Email not exists | Enter fake email | Show email not found | Medium | Negative |
| TC_AUTH_015 | R4 | Logout successfully | Logged in | Click Logout | Session cleared, redirected to login | High | Positive |
| TC_CART_016 | R7 | Search with valid keyword | Products available | Enter "Laptop" | Show matching products | High | Positive |
| TC_CART_017 | R7 | Search with no result | Products available | Enter "UnknownItem" | Show no results message | Medium | Positive |
| TC_CART_018 | R7 | SQL injection in search | Products available | Enter `' OR 1=1 --` | Injection blocked | High | Security |
| TC_CART_019 | R7 | Empty search field | Products available | Submit empty search | Show required keyword message | Medium | Negative |
| TC_CART_020 | R7 | Search special characters | Products available | Enter `#1` | System handles properly | Low | Positive |
| TC_CART_021 | R8 | Filter by valid price range | Products available | Set price 1M–5M | Show correct products | High | Positive |
| TC_CART_022 | R8 | Min price greater than max | Products available | Set Min > Max | Show validation error | Medium | Validation |
| TC_CART_023 | R8 | Min price equals 0 | Products available | Set Min = 0 | Filter works correctly | Medium | Boundary |
| TC_CART_024 | R8 | Filter by category | Multiple categories | Select category | Show correct category products | High | Positive |
| TC_CART_025 | R8 | Negative price input | Products available | Enter -100 | Show invalid price error | Medium | Negative |
| TC_CART_026 | R9 | View product details | Product exists | Click product | Show product details | Critical | Positive |
| TC_CART_027 | R9 | View out-of-stock product | Product out of stock | Click product | Show "Out of stock" | High | Positive |
| TC_CART_028 | R10 | Add product to empty cart | Cart empty | Click Add to Cart | Product added successfully | Critical | Positive |
| TC_CART_029 | R10 | Add same product multiple times | Product in cart | Click Add again | Increase quantity | High | Positive |
| TC_CART_030 | R10 | Add to cart without login | Not logged in | Click Add | Require login or save locally | Medium | Functional |
| TC_CART_031 | R11 | Increase quantity (+) | Product in cart | Click (+) | Quantity updated | High | Positive |
| TC_CART_032 | R11 | Direct input quantity = 99 | Product in cart | Enter 99 | Total updated correctly | Medium | Boundary |
| TC_CART_033 | R11 | Input quantity = 0 | Product in cart | Enter 0 | Show error or remove product | High | Boundary |
| TC_CART_034 | R11 | Enter text in quantity field | Product in cart | Enter "abc" | Show validation error | Medium | Negative |
| TC_CART_035 | R12 | Remove product from cart | Product in cart | Click Remove | Product removed | High | Positive |
| TC_CHK_036 | R13 | Checkout without address | Cart has items | Leave address blank | Show required address error | High | Negative |
| TC_CHK_037 | R13 | Checkout with valid address | Cart has items | Enter valid address | Proceed to payment | High | Positive |
| TC_CHK_038 | R14 | Payment via COD | Address entered | Select COD | Order status Pending | High | Positive |
| TC_CHK_039 | R14 | Payment via valid Visa | Address entered | Enter valid card | Order status Paid | High | Positive |
| TC_CHK_040 | R14 | Payment via invalid Visa | Address entered | Enter invalid card | Payment failed message | High | Negative |
| TC_CHK_041 | R15 | Verify total price calculation | Multiple items in cart | Check total = A + B | Total calculated correctly | Critical | Positive |
| TC_CHK_042 | R15 | Cart cleared after order | Order placed | Open cart | Cart is empty | High | Positive |
| TC_CHK_043 | R16 | View order history | Order exists | Open History | Order displayed | High | Positive |
| TC_CHK_044 | R16 | View order detail | Order exists | Click order detail | Show correct purchased items | Medium | Positive |
| TC_CHK_045 | R16 | History with no orders | No orders | Open History | Show no orders message | Low | Positive |