# Excel Formulas

Use this guide when working with spreadsheet formulas, checking calculation results, or preparing a spreadsheet for review.

## Before Editing Formulas

Before changing formulas, confirm:

- Which sheet, table, or range should be updated.
- Whether the formula should apply to one cell, one column, or a wider range.
- Whether existing formulas nearby already show the expected pattern.
- Whether totals, summaries, charts, or linked sheets depend on the changed cells.

If the impact is unclear, change a small sample first and review the result before applying the formula more broadly.

## Common Formula Checks

### Cell References

Check that formulas refer to the intended cells or ranges.

Look for:

- References that point to the wrong row or column.
- Ranges that stop too early or include extra blank rows.
- Formulas copied from another area without updating references.
- Hidden rows or columns that should or should not be included.

### Relative And Absolute References

When copying formulas, confirm whether references should move with the formula.

Use relative references when each row should calculate from values on the same row.

Use absolute references when every copied formula should keep referring to the same fixed value, lookup table, or assumption cell.

### Totals And Subtotals

For totals, confirm:

- The full intended range is included.
- Header rows are not included as values.
- Blank rows do not split the calculation range.
- Subtotals are not accidentally counted twice.

When totals look wrong, compare the formula range with the visible data range first.

### Lookups

For lookup formulas, confirm:

- The lookup value matches the format used in the source table.
- The lookup table includes the required row or key.
- The return column is the intended result column.
- Duplicate lookup values will not create confusing results.

If a lookup returns a blank or error, check spelling, spacing, number formats, and whether the source table includes the expected item.

## Formula Errors

### Formula Displays As Text

If a formula appears as text instead of calculating:

- Confirm the cell is not formatted as plain text.
- Check that the formula starts with an equals sign.
- Re-enter or refresh the formula after changing the cell format.

### Formula Returns An Error

If a formula returns an error:

- Check whether required source cells are blank.
- Confirm referenced ranges still exist.
- Look for deleted rows, renamed sheets, or changed table headers.
- Review the formula in a nearby working cell and compare the pattern.

### Formula Result Looks Wrong

If the formula calculates but the result seems wrong:

- Check the referenced cells one by one.
- Confirm hidden rows and filtered rows are handled correctly.
- Review whether the formula should include or exclude blank values.
- Compare the result with a manual calculation for a small sample.

## Safe Formula Editing Workflow

1. Save or preserve the current version before making broad changes.
2. Test the formula in one cell or a small sample range.
3. Compare the result with an expected value.
4. Copy the formula only after the sample is correct.
5. Review totals, charts, and summaries that may depend on the changed cells.
6. Ask for review before sharing externally when the spreadsheet affects financial, operational, or customer-facing decisions.

## When To Ask For Review

Ask for review when:

- A formula affects totals, forecasts, invoices, reports, or decisions.
- The same formula will be copied across many rows or columns.
- The spreadsheet contains hidden rows, filters, or linked sheets.
- A lookup formula affects customer-facing or operational output.
- You are not sure whether a reference should be fixed or relative.

## Quick Checklist

Before sharing a spreadsheet that includes formula changes:

- Confirm the formula range is correct.
- Check copied formulas for shifted references.
- Review hidden rows and filtered data.
- Compare at least one result manually.
- Confirm totals and summaries updated correctly.
- Ask for review when the impact is broad or unclear.
