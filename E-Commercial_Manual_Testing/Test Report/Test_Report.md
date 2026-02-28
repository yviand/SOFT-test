# TEST REPORT

## 1. Project Overview
- **Project Name:** Simulated E-Commerce Website  
- **Test Duration:** 1 week (simulation)  
- **Modules Tested:** Authentication, Product & Cart, Checkout  
- **Total Test Cases Designed:** 45  
- **Total Test Cases Executed:** 45  

---

## 2. Test Execution Summary

| Status  | Count | Percentage |
|---------|--------|------------|
| Pass    | 35     | 77.8%      |
| Fail    | 10     | 22.2%      |
| Blocked | 0      | 0%         |

- **Execution Rate:** 100%  
- All planned test cases were executed.

---

## 3. Defect Summary

- **Total Bugs Logged:** 10  

### Severity Breakdown

| Severity | Count |
|----------|--------|
| Critical | 2 |
| Major    | 4 |
| Minor    | 4 |

### Top Critical & Major Defects

1. **BUG_CART_002** – Negative quantity allowed causing negative total price (Critical)  
2. **BUG_CHK_005** – HTTP 500 error when processing invalid Visa payment (Critical)  
3. **BUG_CHK_004** – Cart not cleared after successful checkout (Major)  
4. **BUG_AUTH_001** – Login failure without error message display (Major)  
5. **BUG_CART_003** – Incorrect total calculation (VAT missing) (Major)

---

## 4. Quality Assessment

- Checkout and Cart modules show multiple logic validation issues (boundary and data validation).
- Critical server error (HTTP 500) indicates missing exception handling.
- UI overall stable on desktop; minor display issues observed on mobile view.
- Minor defects mainly related to UI alignment and text formatting.

---

## 5. Release Decision

**Final Decision: NO RELEASE ❌**

### Reasons:
- Test Pass Rate = 77.8% (below required ≥ 95% threshold).
- Open Critical and Major defects affecting payment and order workflow.
- Financial calculation inconsistencies present risk to system integrity.

Release can only be reconsidered after all Critical and Major defects are resolved and regression testing confirms stability.