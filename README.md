# GTU 75% attendance calculator: how many lectures can I miss?

GTU Hero's backlog guide notes that you need at least 75% attendance to fill the GTU exam form and sit the end-semester exam, and that low attendance can cost you the term even with zero backlogs. Attended aur held lectures daalo: ye page batata hai kitne aur bunk kar sakte ho, ya kitne lagatar attend karne padenge to get back to 75%.

Live page: https://princeadvant.github.io/gtu-attendance-75-calculator/

## Formulas

- Attendance % = attended / held × 100
- Can still miss x lectures while attended / (held + x) ≥ 75%: x = floor((100a − 75h) / 75)
- Must attend y lectures in a row: (a + y) / (h + y) ≥ 75%: y = ceil((75h − 100a) / 25)

## Test

`node test.js` checks the formulas against hand-worked values and prints `All checks passed`.

## Tips

- Defaults are own practice values: 45 of 64 is 70.31%, so 12 straight lectures bring it to 57 of 76 = 75%.
- Colleges may count up to 10% absence caused by illness (GTU circular of 2 April 2011, as cited in GTU Hero's guide). Medical certificate time pe jama karo, not after the list is out.
- Your college decides how attendance is counted (per subject, theory and lab separately, and so on). Use this as a planner and confirm the official count with your college.

Detain rules, term grant and exam form status: [GTU Hero backlog rules guide](https://gtuhero.com/blogs/gtu-backlog-rules-atkt-kt-detain-fees) (GTU Hero is my project).
