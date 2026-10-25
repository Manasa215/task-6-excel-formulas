# Task 6 — Excel Formulas & Functions Fundamentals

## Project overview
This project demonstrates common Excel formulas used in entry-level data analytics: `VLOOKUP`, `XLOOKUP`, `IF`, `SUMIFS`, `COUNTIFS`, text functions (`LEFT`, `RIGHT`, `MID`, `TRIM`, `CONCAT`), `IFERROR`, and `INDEX/MATCH`.

**Dataset:** 30 synthetic retail transactions plus a product reference table. Names and email addresses are fictional examples; no personal customer data is used.

## Files
- `Task6_Excel_Formulas_Workbook.xlsx` — primary deliverable with transaction data, product reference, formula practice playground, and interview notes.
- `docs/FORMULA_NOTES.md` — short explanations and formula patterns.
- `docs/ROLLBACK_EVIDENCE.md` — rollback plan and evidence checklist.
- `.github/workflows/workbook-check.yml` — basic repository validation workflow.
- `deployment/DEPLOYMENT.md` — deployment/submission configuration. This is a static workbook project, so no hosted app deployment is required.

## Workbook guide
1. **Transactions**: sample order-level data. The `Sales` column uses `Quantity × Unit Price × (1 − Discount)`.
2. **Product Reference**: product ID, name, category, and list price.
3. **Formula Practice**: formula examples and a live playground on the right. Change the product ID, region, channel, or threshold to test formulas.
4. **Interview Notes**: concise answers to the required interview questions.

## How to test
- Change `H2` on **Formula Practice** to `P1005` and verify the VLOOKUP/XLOOKUP results update.
- Change `H7` or `H8` to test `SUMIFS` and `COUNTIFS` for a different region/channel.
- Set `H15` to `P9999` and verify `IFERROR` displays `Product not found`.
- Test blank input and lookups with text/number mismatches. Excel may treat `"1001"` (text) differently from `1001` (number); normalize the data type and remove extra spaces where needed.
- `XLOOKUP` requires Microsoft 365 or Excel 2021+. If it is unavailable, use `INDEX/MATCH` or `VLOOKUP`.

## Reproducibility and limitations
- The data is synthetic and intended for practice, not business decision-making.
- Formulas are stored in the workbook; formula results may calculate when opened in Excel or Google Sheets.
- The GitHub Actions workflow validates that the expected project files exist. It does not calculate Excel formulas.
- Because this is a workbook deliverable rather than a deployed web service, the deployment configuration documents release and rollback steps instead of hosting an application.

## Submission checklist
- [ ] Upload all repository files to a **public** GitHub repository.
- [ ] Open the workbook from the repository and check that formulas recalculate in your spreadsheet application.
- [ ] Add a screenshot of the workbook to the repository (optional but recommended; do not include personal data).
- [ ] Submit the public repository URL through the internship portal.
- [ ] Publish the LinkedIn post, then add the post URL to the internship portal if requested.
