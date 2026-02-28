# TEST METRICS

## 1. Test Execution Rate
- **Formula:** (Executed Test Cases / Planned Test Cases) × 100
- **Result:** (45 / 45) × 100 = **100%**
- **Pass Rate:** (35 / 45) × 100 = **77.8%**
- **Status:** All planned test cases were executed. However, pass rate indicates remaining stability issues.

---

## 2. Defect Density by Module

| Module | Bugs | Total TCs | Defect Density (Bug/TC) |
|--------|------|-----------|--------------------------|
| Authentication | 2 | 15 | 0.13 |
| Cart & Product | 5 | 20 | 0.25 |
| Checkout | 3 | 10 | 0.30 |

- Checkout and Cart modules show higher defect concentration compared to Authentication.

---

## 3. Severity Distribution

Total Bugs Logged: **10**

| Severity | Count | Percentage |
|----------|--------|------------|
| Critical | 2 | 20% |
| Major | 4 | 40% |
| Minor | 4 | 40% |

- High impact defects (Critical + Major) account for **60%**, indicating core workflow instability.

---

## 4. Requirement Coverage

- **Formula:** (Covered Requirements / Total Requirements) × 100
- **Result:** (16 / 16) × 100 = **100%**
- All requirements (R1 – R16) are mapped with ≥ 2 test cases in RTM.
- No missing requirement traceability detected.