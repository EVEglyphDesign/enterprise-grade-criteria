# EgD GCF Scoring Workbook — build & verification notes

**Deliverable:** `/home/user/workspace/egc/artifacts/EVEglyphDesign_GCF_Scoring_Workbook.xlsx`
**Build script:** `/home/user/workspace/egc/build_gcf_workbook.py` (openpyxl, re-runnable)
**Visual proof:** `/home/user/workspace/egc/artifacts/EVEglyphDesign_GCF_Scoring_Workbook.pdf` (6 pages)
**Logic test copy:** `/home/user/workspace/egc/_gcf_logic_test.xlsx` / `.pdf` (all eight scores = 2, veto 1 = Yes)

## Sheets
1. **Read me** — purpose, four-step method, the 2/1/0 evidence standard (trust-centre page caps at 1), mandatory evidence citation, verdict reading, "not legal advice", licence line (unmodified use with attribution; no rebranding).
2. **Scoring sheet** — SD-1…SD-8, columns B–G (Domain ID | Control domain | What evidenced (2) looks like | Score | Evidence cited | Notes). Score cells `E6:E13` blank, list validation `"0,1,2"`, footer `=SUM(E6:E13)`.
3. **Result** — veto dropdowns `C6:C9` (`"Yes,No"`), total `C11 =SUM('Scoring sheet'!E6:E13)`, unscored `C12 =COUNTBLANK(...)`, verdict `C14`:
   `=IF(COUNTIF(C6:C9,"Yes")>0,"DECLINE — veto condition triggered",IF(COUNTBLANK('Scoring sheet'!E6:E13)=8,"Not yet scored",IF(C11>=14,"Proceed",IF(C11>=10,"Proceed with conditions",IF(C11>=6,"Renegotiate before signature","Decline")))))`
   Conditional formatting fills the verdict cell and any "Yes" veto cell with accent orange #E87722. Blank scores are tolerated (SUM/COUNTIF ignore blanks); an untouched sheet reads "Not yet scored" rather than a false "Decline".
4. **Domain detail** — one block per domain: fuller description plus three written questions for the vendor. Manual page breaks before SD-4 and SD-7 so no block splits across pages.

## Verified
- Reopened with openpyxl: 4 sheets, both data validations present with correct ranges, all four formulas present as strings.
- LibreOffice recalc: 0 errors (`#REF!`/`#VALUE!`/etc.) on both the blank workbook and the filled test copy.
- Veto override tested: total 16 with veto 1 = Yes still returns "DECLINE — veto condition triggered", rendered in orange.
- Rendered all 6 PDF pages as images: no clipped text, no overflow, gridlines off, cream/cream-2/ink/line/mute plus orange accent only — no teal, navy, blue, or default Excel red/green.

Not committed to git.
