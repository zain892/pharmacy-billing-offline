# Pharmacy Billing (Offline)

A simple pharmacy inventory and billing app for a small shop. It is one HTML file. There is nothing to install and no internet is needed.

## Features
- Billing screen with barcode scanner or typed search
- Medicine list with barcode, batch, expiry, buy and sell price, and stock
- Stock goes down automatically after each sale and cannot go below zero
- Discount per bill
- Prints 80mm thermal receipts with the shop name, address and phone
- Reprint old bills
- Daily sales report
- Low-stock and near-expiry alerts (expired or expiring within 60 days)
- Saves data to a folder on the hard disk, with one backup copy per day
- Manual backup and restore (JSON file)

## How to use
1. Download `pharmacy.html` and keep it in one place. Do not move it later.
2. Open it in **Chrome or Edge**. Firefox cannot save to a folder.
3. Click **Choose data folder** and pick a new, empty folder such as `C:\PharmacyData`. Allow access when asked.
4. Go to **Backup & shop** and enter the shop details.
5. Go to **Medicines** and add medicines. Scan the barcode into the barcode box, or type it.
6. Go to **Billing**, scan or search, then click **Save & print bill**.

After opening the app, check that the banner at the top is green before making bills. If it says "NOT SAVING TO DISK", click **Reconnect folder** and allow access.

## Printing (80mm thermal printer)
- Install the printer's Windows driver and print a Windows test page first.
- In Chrome's print dialog choose the printer, paper size 80mm, margins None, scale 100%, and turn off headers and footers.
- For 58mm paper, change `72mm` and `80mm` in the print section of the CSS to `50mm` and `58mm`.

## Barcode scanners
Any USB scanner that types like a keyboard works. Scan a barcode into Notepad first to check.

## Where data is stored
- In the data folder you chose: `pharmacy-data.json`, plus `backup-YYYY-MM-DD.json` once a day.
- Also inside the browser's own storage as a second copy.
- If the browser's data is cleared, open the app, choose the same folder, and the data reloads.
- Copy the folder to a USB drive regularly in case the hard disk fails.

## Limitations
- Chrome or Edge only for folder saving.
- Chrome may ask for permission again after the browser restarts.
- No user logins, no multiple computers sharing one database, no supplier or purchase records.
- Bills are kept forever, so a very busy shop may eventually fill the browser's storage. Use the daily backup files to keep records.
- Prices are in PKR. The receipt text is in English.
- Not tested with every scanner or printer model. Test with a few bills before real use.

## Disclaimer
This is a simple tool for small shops. It is not certified accounting or pharmacy software. Keep your own backups and check stock and totals yourself.

## License
MIT
