# Sprivo Clean Sheet — Beta v0.1

Turn a messy bank or credit-card CSV into a clean file you can upload to **QuickBooks Online**.
Free. Your file never leaves your computer.

> **Beta v0.1: an early version.** It has been tested on made-up sample files that imitate common bank and card exports. It has **not** yet been checked against real files from many banks or against a real QuickBooks upload. **Check the result before importing it into QuickBooks.** No warranty; see the end of this page.

## Use it

- **In your browser:** <https://sprivoofficial.github.io/clean_csv/>
- **Offline:** download `clean-sheet.html` from [Releases](https://github.com/sprivoofficial/clean_csv/releases/latest), then double-click it. It opens in your browser and works with no internet.

Inside the page it is called **Clean Sheet**.

## How it works

1. Drop the CSV from your bank or card (or press **Try a sample file**).
2. Clean Sheet tidies it and shows what it did. Press **See before / after** to compare.
3. Answer the few questions it asks (for example "Flip signs?" for credit-card files). When something could mean two things, it asks and never guesses.
4. Press **Download for QuickBooks**. You get a file with 3 columns (`Date, Description, Amount`) or 4 columns (`Date, Description, Credit, Debit`). Files over 1,000 rows are split for you.

When QuickBooks asks for the date format during upload, choose the one shown next to the download button.

## What it handles

- `.csv` or `.txt` files (commas, semicolons, tabs or pipes), in UTF-8, UTF-16 or Windows-1252
- Checking, savings and credit-card exports in the usual layouts: one Amount column, or separate Debit and Credit columns
- Title lines, blank rows, repeated headers and total rows (they are set aside and listed, never silently dropped)
- Mixed date styles, and amounts like `$1,234.56`, `(12.50)`, `45.00 DR`, `45.00-`
- Credit-card files that show purchases as positive numbers (you confirm the sign)
- Files with two dates (transaction and posting): it asks which one to use
- **Experimental:** PayPal and Wise exports (checked against sample files published online); Stripe-style exports (layout not yet checked against a real Stripe file)

## What it does not handle

Excel `.xlsx` files (export the sheet as CSV first), PDF statements, QBO and OFX files, files that are not in English, files that combine several accounts, and QuickBooks Desktop (this makes files for QuickBooks Online). If a file has several currencies, you pick one at a time.

## Privacy

Everything happens inside your browser tab. Nothing is uploaded or saved, and the page tells your browser to block all network connections. It loads nothing from other sites: no ads, no trackers, no accounts. You can switch off your internet and it keeps working.

## Feedback

Use the **Report a problem** link at the bottom of the page, or open an issue here. **Do not send or paste real statements or account numbers.** Describe the layout instead: the column names and one or two made-up rows.

## License and disclaimer

Copyright © 2026 Sprivo. All rights reserved. You may use Clean Sheet for free as provided; you may not copy, modify, redistribute or sell it without permission.

Clean Sheet is provided "as is", without warranty of any kind. It is an early version and can make mistakes. You are responsible for checking the result before using it in your accounts. Sprivo Clean Sheet is an independent tool and is not affiliated with or endorsed by Intuit or QuickBooks.
