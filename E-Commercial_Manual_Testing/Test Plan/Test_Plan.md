# TEST PLAN

## 1. Overview
This document outlines the objectives, scope, strategy, resources, and schedule for testing the simulated E-Commerce Website.  
The goal is to validate core modules (R1 – R16) and ensure system stability before release.

---

## 2. Scope

### In-Scope
**Module A – Authentication**
- User registration
- Login / Logout
- Forgot password

**Module B – Product & Cart**
- Product search
- Filter by price/category
- View product details
- Add to cart
- Update quantity
- Remove item from cart

**Module C – Checkout**
- Enter shipping address
- Select payment method (COD / Mock Visa)
- Place order
- View order history

### Out-of-Scope
- Performance testing
- Load/Stress testing
- Automation testing
- Advanced security penetration testing

---

## 3. Test Strategy

- **Functional Testing:** Validate business logic, main flows, alternative flows, and error handling.
- **Basic UI Validation:** Verify layout, input validation, and error messages.
- **Smoke/Regression Testing:** Ensure bug fixes do not impact existing features.

---

## 4. Test Environment

- **Device:** Personal PC/Laptop
- **Browser:** Google Chrome (latest version)
- **Operating System:** Windows 10 / Windows 11
- **Test Data:** Predefined valid/invalid accounts, mock payment information

---

## 5. Entry & Exit Criteria

### Entry Criteria
- Test environment ready
- Requirements (R1 – R16) finalized
- Test Cases & RTM completed and approved

### Exit Criteria
- 100% planned Test Cases executed (45+ TCs)
- No open Critical or Major defects
- Test Pass Rate ≥ 95%

---

## 6. Risks & Mitigation

| Risk | Impact | Mitigation |
|------|--------|------------|
| Requirement changes during testing | High | Update Test Cases & RTM immediately |
| High number of defects causing delay | Medium | Prioritize critical flows, daily bug tracking |
| Test environment instability | Low | Coordinate with Dev/Ops, review test artifacts meanwhile |

---

## 7. Roles & Responsibilities

- **QA Lead**
  - Prepare Test Plan
  - Monitor progress
  - Review defects
  - Approve release readiness

- **Manual QA**
  - Design Test Cases
  - Maintain RTM
  - Execute tests
  - Report and retest defects

---

## 8. Test Schedule

| Phase | Activity |
|-------|----------|
| Phase 1 | Requirement analysis & Test Planning |
| Phase 2 | Test Case & RTM design |
| Phase 3 | Test Execution & Bug Reporting |
| Phase 4 | Regression Testing & Test Report |