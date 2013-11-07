Spreadsheets.AutoFuel
=====================

A simple spreadsheet for tracking gas purchases and keeping track of your car's fuel efficiency.

![Gas.xlsx Spreadsheet](https://raw.github.com/ernesthwang/Spreadsheets.AutoFuel/master/doc/images/Screenshot01.png "Gas.xlsx Excel Spreadsheet")


## How to use this spreadsheet

### Change the spreadsheet tab name

This can be found at the bottom of the Excel window.  It is initially set to "YOUR CAR'S YEAR-MAKE-MODEL HERE", so change it to match your car's description (for example: "2011 Nissan Pathfinder").

### Fill out your initial odometer reading

Row 3 contains the initial state of your car when you first start tracking your milage.  Fill out the inital odometer reading in the white cell (C3).  All other (amber) cells should be seeded at zero.

### Fill out the data from your first gas fill up

When you first fill up your tank after initializing this spreadsheet, you will fill out the white cells in row 4.  Input the following:
* Date of purchase
* Your current odometer reading
* The number of gallons/liters used
* The price per gallon/liter
* In the Notes column, describe your driving pattern since your last fill up (optional).  For example, you might want to add a special note if you took a long trip since the last fill up.

### Fill out the data from your other fill ups
* Copy the last line of the spreadsheet to the line below it.  The formulas should automatically reference the correct adjacent cells.
* Enter the same types of data as with the first fill up (i.e. overwrite the white cells with the pertinent data)


## General notes
* You should only be filling out the white cells in the spreadsheet (columns A, C, E and G)
* The blue cells should be formulas that are copied from row 4.  Don't hand enter values from these columns.

## What to observe

The notable things to observe from this spreadsheet are as follows:

### Total since tracking fuel
* Total days driven: B1
* Average miles/km driven per day: C1
* Total miles/km driven: D1
* Total gallons/liters used: E1
* Average miles/gallon or km/liter: F1
* Average price of fuel: G1
* Total amount spent on fuel: H1

### Current fill up
* Days since last fill up: Column B
* Miles/km driven since last fill up: Column D
* Miles/Gallon / km/L for the last fill up: Column F
* Amount spent for current fill up


## If you are not American

If you live in a country that doesn't use Dollars, miles or gallons, just change the values to fit your needs.  You will need to change the column headers as well as the column formatting.  The calculations should work the same.

## Cell formulas

| | A | B | C | D | E | F | G | H |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **1** | | `=SUM(B3:B1048576)` |`=D1/B1` | `=SUM(D3:D1048576)` | `=SUM(E3:E1048576)` | `=D1/E1` | `=H1/E1` | `=SUM(H3:H1048576)` |
| **2** | **Date** | **Days** | **Odometer Reading** | **Driven** | **Amount Filled** | **MPG** or **km/L** | **Total** |
| **3** | *Date you started tracking* | 0 | *initial reading* | 0 | 0 | 0 | 0 |
| **4** | *Date of your first fill up* | `=A4-A3` | *your reading* | `=C4-C3` | 0 | `=D4/E4` | 0 | `=G4*E4` |
| **5** | *Date of your second fill up* | `=A5-A4` | *your reading* | `=C5-C4` | 0 | `=D5/E5` | 0 | `=G5*E5` |

