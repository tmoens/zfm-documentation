## Users

Terminology first.

The system wants to associate a *researcher* with each stock.

Researchers come and go at a facility, so there are numerous situations where
a stock is associated with a researcher who has left.
But the system keeps a record for that researcher.

For better or for worse, the researchers are listed in the *user* table in
the database.
When the researcher is at the lab, that user is *active* and when they leave, the user
is designated as *inactive*.

So for migration, we need to get a list of all *researchers* - present and past - who
have ever worked in the lab (or at least, any researcher that is to be associated
with any stock) and put those researchers in the *user* table.
We designate the old researchers as inactive, and we can give them fake email addresses.

For the migration process, you will probably be given a list of stocks and
for each stock, there will be a researcher or "owner" name.
A name may show up with several variations (Mary, MaryMullins, MaryM, MM).
Best is to copy the column of researchers, remove duplicates, put the list in
the migration spreadsheet and send the migration spreadsheet to the customer
to fill in the details.

After that, you can build a table which translates from any particular
researcher string you are given to the specific researcher name.

So, for example the researcher may be Allison Lastra, and you create a user called
allison.lastra.
In the stockbook you are given, she shows up as "Allison" and "Allison L" and "APL".
In the spreadsheet you build a table that has the mappings:
- Allison => allison.lastra
- Allison L => allison.lastra
- APL => allison.lastra

Then when on the import stock sheet you map from the given string (e.g. Allison L) to
the correct user with the aid of the translation table you built.

