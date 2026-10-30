# POS System (GitHub Pages)

A web POS that reads its menu from an Excel file. Main language: English. Optional Mizo labels.

## Files
- `index.html` – the POS website
- `menu.xlsx` – menu data (sheets: Menu, Options, Labels, README)

## Deploy on GitHub
1. Create a new repository (e.g. `my-pos`).
2. Upload `index.html`, `menu.xlsx`, `README.md` to the root.
3. Settings → Pages → Deploy from a branch → `main` / `(root)` → Save.
4. Wait 1–2 minutes: `https://<username>.github.io/my-pos/`

## Daily workflow
1. Pick a category, tap menu items (Stir-fry / Soup ask for Pork, Chicken or Seafood).
2. Choose **Order taken by**, add a note if needed.
3. **Save Bill** – the bill is stored as *unpaid* (see it under **Open bills**).
   Or **Save & Pay** to pay straight away.
4. Later: **Open bills → Pay** → choose Cash or Transfer, cashier, confirm.
   From Open bills you can also **Edit** (add/remove items) or **Cancel bill** (kept in history as Void).

## Starter menu (Thai Special Menu, prices in Rs)
- **Stir-fry:** F01 1 Mama Spicy, F02 Chicken Wing, F03 3 Fried Glass Noodles, F04 Tom Yam Fried Rice, F05 Cashewnut Fried Rice, F06 Steam Fish Limestone
- **Soup:** S01 Mama Tom Yam Noodle, S02 Tom Yam Sea Foods
- **Salad:** SA01 Pork Slice Salad, SA02 Chicken Salad, SA03 Papaya Salad (Regular 100 / With Prawn 160)
- **Mizo Foods:** MF01 Chaw Pangngai, MF02 Chaw Te, MF03 Sabuti (Small 50 / Large 100), MF04 Veg Chow, MF05 Egg Chow, MF06 Veg Rice, MF07 Egg Rice, MF08 Omelette
- **Drink:** D01 Lassi, D02 Coffee, D03 Thingpui
- Every category has **10 slots**. A slot with a blank name is reserved and hidden – type a name and price (Admin or Excel) to switch it on.
- **Variants** = choices with their own price (e.g. Small 250 / Large 350). Excel sheet `Variants`, or Admin → Variants column (`Small=250, Large=350`).

## Admin (menu editing)
Press **🔒 Admin** and enter the PIN (default `1234` – change it in Admin → Settings).
- Edit item names, prices, variants, categories, codes; turn meat options on/off per item.
- **＋ Add menu item** (a new code such as F11 / S11 / D11 is created automatically) and delete items.
- Edit meat options and their extra price.
- Type Mizo labels (Admin → Languages).
- Import / download `menu.xlsx`, reset to the GitHub version, delete history.

Notes
- Edits are saved **in that browser**. To make them permanent on every device: Admin → *Download menu.xlsx* → upload it to GitHub (replace the old file) → Admin → *Reset to menu.xlsx*.
- The PIN is a convenience lock only. This is a static website, so it is not real security.

## Language
Use the **EN / Mizo** buttons at the top. Mizo text comes from the `Labels` sheet (column C) or Admin → Languages. Blank labels show in English.

## Codes
`F01–F10` Stir-fry · `S01–S10` Soup · `SA01–SA10` Salad · `MF01–MF10` Mizo Foods · `D01–D10` Drink · `OPEN` Open item

## Sales data
- Stored in the browser of the device in use (localStorage).
- **Export sales (.xlsx)** gives sheets: Sales (every line), Bills (one row per bill), Summary (paid only).
- Export regularly – clearing browser data deletes sales.
