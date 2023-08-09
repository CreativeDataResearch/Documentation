# Preface

Before “getting started” with DAC Accounts Payable (A/P) System, users should refer to the Introduction of the Getting Started document for information about DAC data, screens and menus.

![Alt text](/images/AP_mainmenu.png)

After selecting option 11 (Accounts Payable) of the DAC Main Operations Menu screen, the Accounts Payable screen appears.

![Alt text](/images/AP_APMenu.png)

Users can press \<F3> to redisplay the Main Operations Menu screen.

Refer to the [Accounts Payable Quick Reference Guide](<../DAC Refrence Guides/Accounts Payable QRG.md>) for an overview of the use of the Accounts Payable System.

For information about transferring purchase orders to Accounts Payable, and the report which is printed when transfers occur, refer to Transferring Purchase Orders To Accounts Payable of the Purchasing document.

## Getting started with Accounts Payable

The steps below are followed to create the necessary records before the Accounts Payable System is used. If the DAC General Ledger System is used (or only the General Ledger account numbers are used), the steps below must not be taken until:

- The cost center number(s) and General Ledger account numbers are defined. Refer to the General Ledger document for information about using the G/L File Maintenance applications to add cost center and G/L account records.

- The cost center number(s) and General Ledger account numbers are combined using the Work With Cost Center application.

>Note: The General Ledger System is used by selecting option 22 (General Ledger) of the Accounts Payable screen, or by selecting option 12 (General Ledger) of the DAC Main Operations Menu screen.

**Step 1**: Use the Work With System Options application to make any necessary changes to the value of the default system option record fields related to Accounts Payable. Refer to the DAC Default System Options document for information about the A/P Interface Active? and A/P Terms Positions Used fields of the SYS005 default system option, and the Accounts Payable Active? field of the SYS015 default system option.

**Step 2**: Use the Company Maintenance screens to add preliminary data, such as name and address, of the company. Multiple companies must be set up if users track retained earnings or net profit and loss for more than one entity, such as multiple warehouses or divisions. Refer to Working With Company Records for additional information.
>Note: This step is not necessary if the company records were previously added using the General Ledger System.

**Step 3**: Use the User Profile Maintenance screen to designate the names of A/P users, and with which company each user works. Refer to Working With User Profile Records for additional information. >Note: This step is not necessary if the user profile records were previously added using the General Ledger System.

**Step 4**: Sign off the DAC system, then sign back on.

**Step 5**: Use the Company Maintenance (A/P) screen to add company A/P data, such as the aging method used by a company. Refer to Working With Company A/POptions for additional information.

**Step 6**: Use the Company Maintenance (G/L) screen to add company G/L data if General Ledger account numbers are used. Refer to Working With Company G/L Options for additional information.
>Note: This step is not necessary if the company G/L options were previously added using the General Ledger System.

**Step 7**: Use the Period Date Maintenance screen to add period date data. Refer to [Working With Period Date Records](#working-with-period-date-records) for additional information.
>Note: This step is not necessary if the period date records were previously added using the General Ledger System

**Step 8**: Use the Period Date Inquiry screen to verify the starting and ending dates of the periods (also referred to as months) of the user’s fiscal year. Refer to Displaying Period Date Records for additional information.

**Step 9**: Use the Period Status Inquiry screen to verify the A/P open status for the periods of the user’s fiscal year. Refer to Displaying Period Status Records for additional information.

**Step 10**: Contact CDR support personnel who will assist users with the execution of the Company A/P One Time Maintenance application.

**Step 11**: Use the Bank Maintenance screen to add bank data. Refer to Working With Bank Records for additional information.

**Step 12**: Use the Vendor Terms Maintenance screen to add terms data. Refer to Working With Terms Records for additional information.

**Step 13**: Use the Vendor Maintenance screen to add vendor data. Refer to Working With Vendor Records for additional information.

**Step 14**: Use the Item Maintenance screen to add A/P item data. Refer to Working With A/P Item Records for additional information.

**Step 15**: Use the Work With A/P Options screen to designate various defaults (company, terms, bank and pay date) and A/P related options. Refer to Working With A/P Options for additional information.

**Step 16**: Use the Vendor Maintenance screen to add data concerning recurring payments. Refer to [Working With Recurring Invoice Records](#working-with-recurring-invoice-records) for additional information.
>Note: The Special Item application (option 4 of the A/P File Maintenance screen) and Entity application (option 10 of the A/P File Maintenance screen) are no longer used due to system upgrades.

Refer to the [Accounts Payable Quick Reference Guide](/Quick%20Reference%20Guide/Accounts%20Payable%20Quick%20Reference%20Guide.md) for an overview of the use of the Accounts Payable System

## Accounts Payable and General Ledger Account Numbers

If the DAC General Ledger (G/L) System is used, credit and debit journal entries are created when invoice batches are posted and payments are processed.

### Posting invoice batches

The General Ledger account number which is credited when invoice batches are posted is designated by the A/P account number field (see below) of the company A/P options

![Alt text](../../images/AP_CompanyMaintenanceAP.png)

Refer to Working With Company A/P Options for additional information.

The various G/L account numbers which are debited when invoice batches are posted are designated by a user-named field (see below) of the A/P item records. Refer to Working With A/P Item Records for additional information
![Alt text](../../images/AP_ItemInquiry.png)

>Note: The specific name of this A/P item record field is designated by the value of the **Account header** field (see below) of a company’s G/L options. Refer to Working With Company G/L Options for additional information.

![Alt text](../..//images/AP_CompanyMaintenanceGL.png)

When invoice batches are posted, a single debit journal entry is created in G/L for each detail line of an invoice.
Refer to Working With Company A/P Options for information about the:

- **Inv jrnl entry method** field which is used to designate if a single credit journal entry is created for each invoice of a batch, or for the entire batch.

- Dates used for debit and credit journal entries when posting invoice batches.

### Processing Payments

Payment processing includes:

- Using the Print Checks application to print checks for a payment batch.
- Using the Process Manual Payments application to enter data concerning payments made with hand-written checks.
- Using the Process EFT Payments application to enter data concerning payments made with electronic funds transfers (EFTs).

The General Ledger account number which is debited when payments are processed is designated by the A/P account number field (see below) of the company A/P options.

![Alt text](../../images/AP_CompanyMaintenanceAP.png)

Refer to Working With Company A/P Options for additional information. The G/L account numbers which are credited when payments are processed (also referred to as the cash account number and the discount number) are designated by the following fields:

- **Cost Center** and **G/L Account** # fields (see below) of the bank records. Refer to Working With Bank Records for additional information.

    ![Alt text](../../images/AP_BankMaintenance.png)

>Note: The specific names of these bank record fields are designated by the values of the Cost cntr hdr and Account header fields of a company’s G/L options (as described above)

- **Discount account** field (see below) of the company A/P options.

    ![Alt text](../../images/AP_CompanyMaintenanceAP.png)
Refer to Working With Company A/P Options for additional information.

When payments are processed, a single credit journal entry is created in G/L (for both the cash account number and the discount number) for each individual payment (printed check, manually-written check and EFT transaction).

Refer to [Working With Company A/P Options](#working-with-ap-options) for information about the:

- **Pmt jrnl entry method** field which is used to designate if a single debit journal entry is created for each payment of a batch, or for the entire batch when printing checks.
        >Note: A single debit journal entry is created for each manual check and each EFT processed.

- Dates used for debit and credit journal entries when processing payments.

# Working with Accounts Payable File Maintenance

The Accounts Payable File Maintenance applications are used to create:

|  |  |
| :---: | :---: |
| **Company Records**   | **Terms Records** |
| **User Profile Records**   | **Vebdor Records**|
| **Company A/P Options**  | **A/P Item Records** |
| **Company G/L Options**  | **A/P Options** |
| **Period Date Records**  | **Recurring Invoices Records**|
| **Bank Records**|  |
| | |

After selecting option 11 from the Main Operations Menu screen, the Accounts Payable screen appears.

![Alt text](../../images/AP_APMenu.png)

After selecting option 20 (A/P File Maint.) from the Accounts Payable screen, the A/P File Maintenance screen appears.

![Alt text](../../images/AP_APFileMaintenance.png)

## Working With Company Records

The Company Maintenance screen is used to add at least one company record before the Accounts Payable System is used. Multiple companies must be set up if users track retained earnings or net profit and loss for more than one entity, such as multiple warehouses or divisions. Refer to [Working With Company G/L Options](#working-with-company-gl-options) for additional information.

![Alt text](../../images/AP_APFileMaintenance.png)

1. Select option 7 (Company) from the A/P File Maintenance screen. The Company Maintenance (Change) screen appears.

    ![Alt text](../../images/AP_CompanyMaintenance.png)

2. If necessary, enter ? for the **Company** (3,a) field and press \<Enter> to display a list of the previously added company records on the Company Selection screen.If desired, 1 (Select Request) can be entered in the selection column to display, edit or delete a company record, or the user can press \<F3> to display the Company Maintenance (Add) screen.

3. If necessary, press \<F9> (Go to 'Add' mode) to display the Company Maintenance (Add) screen.

4. To add a new company record, enter a company code for the **Company** (3,a) field.

5. Press \<Enter>. The Company Maintenance screen is redisplayed.

6. Enter data for the following fields:\
    • **Name** (40,a) - the name of the company.\
    • **Address line 1** (30,a) - the company’s street number and street name, or post office box number.\
    • Optional: **Address line 2** (30,a) - remaining portion of the company’s address, such as post office box number if not entered for Address Line 1.\
    • **City** (20,a) - the city of the company’s mailing address.\
    • **State** (2,a) - the state of the company’s mailing address.\
    • **Postal code** (5-9,n) - the zip code and 4-digit extension of the company’s mailing address.\
    • Optional: **Phone number** (10,n) - the company’s area code and telephone number.\
    • Optional: **Fax number** (10,n) - the company’s area code and telephone number for fax transmission\

7. Enter Y (yes) for the **G/L interface** (1,a) field to designate that Accounts Payable data is transferred automatically to General Ledger. If the DAC General Ledger System is not used, enter N (no).
    >Note: If the General Ledger System is not used, but chart of account numbers that are created using the General Ledger System are used, Y must be entered for the **G/L interface** field.

8. Press \<Enter> when prompted to confirm. The Record added message appears at the bottom of the Company Maintenance screen.

9. Press \<F3> to exit. The A/P File Maintenance screen appears.\
Refer to Working With General Ledger Reports of the General Ledger document for information about printing a complete list of companies.

## Working With User Profile Records

After company records are added, the User Profile Maintenance screen is used to add user profile records which designate the company with which each user works. The designated company will be automatically selected when a user signs on.

Refer to [Selecting An Alternative Company](#selecting-an-alternative-company) for information about using the Select Alternative Company application to work with a different company.

Refer to [Selecting The Default Company](#selecting-the-default-company) for information about using the Select Default Company application to resume working with the default company when work with an alternative company is complete.

1. Select option 11 (User Profile) from the A/P File Maintenance screen. The User Profile Maintenance (Add) screen appears without values for the **User, User name, Cmp** and **Company name** fields if no user profile records have been added.
2. If necessary, press \<F9> (Go to 'Add' mode) to display the User Profile Maintenance (Add) screen.
3. Enter data for the following fields for each user:
• **User** (10,a) - the username which the user enters to sign on the system.\
• **User name** (30,a) - the user’s name.\
• **Cmp** (3,a) - a company code designating the user’s default company. If necessary, enter ? and press \<Enter> to select a company code from the Company Selection screen.\
    >Note: If the value of the **Cmp** field is later changed in the user profile record of a user who is currently signed on, that user must sign off and sign on before the change takes affect.

4. Press \<Enter> and \<F9> (Go to 'Change' mode) when data entry is complete. The User Profile Maintenance (Change) screen appears.
5. To delete a user profile record, enter 4 (Delete request) in the selection column of the desired record, and press \<Enter>. Press \<Page Down> or use the User restrictor field at the top of the screen to locate the desired record.

6. Press \<F3> to exit. The A/P File Maintenance screen appears.
  
### Selecting An Alternative Company

After a user signs on, the Select Alternative Company application can be used to work with a company other than the user’s default company.\

Refer to [Selecting The Default Company](#selecting-the-default-company) for information about using the Select Default Company application to resume working with the default company when  work with an alternative company is complete.

1. Select option 6 (Select Alternative Company) from the A/P File Maintenance screen. The Select Alternative Company screen appears.
2. Enter 1 (Select) in the selection column next to the company code of the desired company, and press \<Enter>. The Your current company code is now \### message appears designating the alternative company selected.
3. Press \<F3> to exit. The A/P File Maintenance screen appears.

### Selecting The Default Company

After working with an alternative company, the Select Default Company application is used to resume working with the user’s default company. Refer to [Working With User Profile Records](#working-with-user-profile-records) for information about designating each user’s default company.

Select option 7 (Select Default Company) from the Accounts Payable screen. The The default company has been selected message appears.

## Working With Company A/P Options

After company records are added, the values of several A/P options must be designated for each company.

If necessary, the Select Alternative Company application can be used before working with company A/P options to allow the user to work with a company other than the user’s default company. Refer to [Selecting An Alternative Company](#selecting-an-alternative-company) for additional information.

1. Select option 7 (Company) from the A/P File Maintenance screen. The Company Maintenance screen appears.
2. Enter the company code of the desired company and press \<Enter>, or enter ? for the Company field and press \<Enter> to select a company from the Company Selection screen.
3. Press \<F16> (\<Shift> plus \<F4>). The Company Maintenance (A/P) screen appears.
4. Enter one of the following values for the A/P aging method field:\
  
     - I designates that A/P aging is based on the invoice date. For example, if an invoice is dated November 1 with 30-day terms, the invoice is considered 1 day past due on December 2.
     - D designates that A/P aging is based on the invoice due date. For example, if the due date is November 1 with 30-day terms, the invoice is considered 31 days past due on December 2.
     - P designates that A/P aging is based on the posting date. For example, if the posting date is November 1 with 30-day terms, the invoice is considered 31 days past due on December 2.

    The aging method is used to produce the A/P cash forecast report (entitled Vendor Aging Summary), and used to calculate the aging figures which appear on the Vendor Account Inquiry (Display) screen.
5. Enter the number of days past the date on which an invoice no longer has a remaining balance for the **Days to hold closed A/P** (3,n) field. The recommended value is 30. It designates how long invoice records and payment records remain in the A/P current files. After this time elapses, the records are automatically saved in A/P history files when the Month End Close application is used.
6. Enter data for the following fields as necessary:
    - **A/P aging bucket 1 name** - a description of the first aging bucket, such as Current.
    - **A/P aging bucket 1 days** - the number of days which an invoice cannot exceed to be included in the first bucket.
    - Optional: **A/P aging bucket 2 name** - a description of the second aging bucket, such as 31 to 60.
    - Optional: **A/P aging bucket 2 days** - the number of days which an invoice cannot exceed to be included in the second bucket.
    - Optional: **A/P aging bucket 3 name** - a description of the third aging bucket, such as 61 to 90.
    - Optional: **A/P aging bucket 3 days** - the number of days which an invoice cannot exceed to be included in the third bucket.
    - Optional: **A/P aging bucket 4 name** - a description of the fourth aging bucket, such as 91 - 120.
    - Optional: **A/P aging bucket 4 days** - the number of days which an invoice cannot exceed to be included in the fourth bucket. Note: When using the Vendor Account Inquiry application to display four columns of aging figures, the amount calculate for the fourth bucket is combined with the fifth bucket, and displayed in the far right column of the screen.
    - Optional: **A/P aging bucket 5 name** - a description of the fifth aging bucket, such as 121+.
    - Optional: **A/P aging bucket 5 days** - enter 999 for the number of days which an invoice cannot exceed to be included in the fifth bucket. Note: When using the Vendor Account Inquiry application to display four columns of aging figures, the amount calculate for the fifth bucket is combined with the fourth bucket, and displayed in the far right column of the screen.
The values of the A/P aging fields are used to produce the A/P cash forecast report (entitled Vendor Aging Summary), and used to calculate the aging figures which appear on the Vendor Account Inquiry (Display) screen.
7. Enter Y (yes) for the **Allow discount override** field to enable the user to changethe values of the **Discount** and fields of the A/P Invoice Posting (Add) and (Change) screens, and the **Discount** field of the Payment Detail Maintenance screen. Refer to Adding An Invoice Batch, Adding A Payment Batch, Working With Manual Payments, and Working With EFT Payments for additional information.
8. Enter Y (yes) for the **Allow detail payment change** field to enable changing the amount of a payment when selecting invoices for payment.
9. Enter *1* for the **Number of leader checks** field to designate that the first check loaded in the printer is used when checks are printed. If a single check is “wasted” every time checks are printed, enter *2* for this field. If the first two checks are not used every time checks are printed, enter *3* for this field.
10. Enter one of the following values for the Inv jrnl entry method field:

    - *B* designates that a single credit journal entry is created in General Ledger for the entire batch when an invoice batch is posted in Accounts Payable. Refer to Adding An Invoice Batch for information about using the Posting date field to post entries to the General Ledger.
    - *I* designates that a credit journal entry is created in General Ledger for each invoice when an invoice batch is posted. Refer to Adding An Invoice Batch for information about using the Inv date field to post entries to the General Ledger.

11. Enter one of the following values for the Pmt jrnl entry method field:
    - *B* designates that a single debit journal entry is created in General Ledger for the entire batch when a payment batch is posted in Accounts Payable.
    - *C* designates that a debit journal entry is created in General Ledger for each payment when a payment batch is posted.\

    Refer to [Working With A/P Options](#working-with-ap-options) for information about using the A/P Check field to designate which date is used for posting entries to the General Ledger.

12. Optional: Enter *Y* (yes) for the Reprint check numbers on preprinted checks field to print check numbers on checks that are pre-numbered, and verify that the correct check is being printed on the correct form.
13. If *Y* (yes) is entered for the G/L interface field of the company’s record, data may be entered for the following fields:
    - **A/P account number** - the cost center number and the liability account number which are credited when invoices are posted and debited when payments are made. Refer to Posting An Invoice Batch and Printing Checks And Check Register for additional information. The cost center number entered for the **A/P account number** field is also used as the default value when adding recurring invoice records and adding invoice batches. Refer to Working With Recurring Invoice Records and Adding An Invoice Batch for additional information.
    - **Discount account** - the cost center number and the expense or income account number used for crediting discounts when payments are made.

    Refer to Working With Company Records for additional information about the **G/L interface** field. Refer also to Working With A/P Item Records for information about the **G/L Account** # field, and to Working With Bank Records for information about the **Cost Center** and **G/L Account** # fields.

14. Press \<Enter> when data entry is complete. The *Record added* message appears at the bottom of the Company Maintenance screen.
15. Press \<F3> to exit. The A/P File Maintenance screen appears.

### Working With Company G/L Options

After company records are added, the values of several G/L options must be designated for each company if G/L account numbers are used. If necessary, the Select Alternative Company application can be used before working with company G/L options to allow the user to work with a company other than the user’s default company. Refer to Selecting An Alternative Company for additional information.

1. Select option 7 (Company) from the A/P File Maintenance screen. The Company Maintenance screen appears.

2. Enter the company code of the desired company and press \<Enter>, or enter ? for the Company (3,a) field and press \<Enter> to select a company from the Company Selection screen.
3. Press \<F15> (G/L). The Company Maintenance (G/L) screen appears.

    If the value of the **Company** field is changed (as illustrated above), the Select Alternative Company application must be used before continuing to work with the Company Maintenance (G/L) screen. In this case, press \<F3> to exit, and refer toSelecting An Alternative Company for additional information.

    If the value of the Company field is unchanged (as illustrated above), continue with the steps below to enter values for the fields of the Company Maintenance (G/L) screen.

4. Enter the text designating the company’s cost centers, such as *Cost Center*, for  the **Cost cntr hdr** (12,a) field. This text will appear as a field name on various  A/P System screens (see the Bank Maintenance screen below), and as a column  heading on various A/P System reports. Refer to the example of the A/P-G/L  Transaction Register in the Posting An Invoice Batch section of this document.
  
5. Enter the text designating the company’s General Ledger account numbers, such  as G/L Account #, for the **Account header** (15,a) field. This text will appear as  a field name on various A/P System screens (see the Bank Maintenance screen  below), and as a column heading on various A/P System reports. Refer to the  example of the A/P Invoice Transaction Register in the Posting An Invoice Batch  section of this document.

6. Enter data for the following fields:

- Optional: **Suspense cost center/account** - the cost center number (3+4,n) and  the account number (5+4,n) used for the suspense total.
- Optional: **Ret. earnings cost cntr/account** - the cost center number (3+4,n)  and the account number (5+4,n) used for the retained earnings total.
- Optional: **Profit/loss cost cntr/account** - the cost center number (3+4,n) and  the account number (5+4,n) used for the net profit/loss total.

7. Press \<Enter> when data entry is complete. The *Record added* message appears at  the bottom of the Company Maintenance screen.

8. Press \<F3> to exit. The A/P File Maintenance screen appears.

In the example below, the field names **Cost Center** and **G/L Account #** appear on the Bank Maintenance screen because the values Cost Center and G/L Account # are entered for the **Cost cntr hdr** and **Account header** fields of the Company Maintenance (G/L) screen.

### Working With Period Date Records

### Working With Bank Records

### Working With Terms Records

### Working With Vendor Records

#### Vendor Record Worksheet

### Working with A/P Item Records

### Working with A/P Options

### Working With Recurring Invoice Records

## Working With Vendor Invoices

### Adding An Invoice Batch

#### Calculating An A/P Allowance

#### Printing Multiple Refrence Lines

### Editing An Invoice Batch

#### Invoice Entry Edit List

### Adding A Credit Memo

### Posting An Invoice Batch

#### A/P-G/L Trans Register

#### Invoice Entry Edit List

#### A/P Invoice Transaction Register

### Adjusting A Posted Invoice

#### A/P Debit/Credit G/L Journal Register

## Working With Payments

### Adding A Payment Batch

#### Reconciling Pay Dates And Periods

### Editing A Voucher

### Editing A Payment Batch

#### A/P Payment Edit List

### Accepting A Payment Batch

#### A.P Payment Check Date Edit Report

### Deleting An Accepted Payment Batch

#### A/P Payment Edit List

## Working With Printed Checks

### Printing Checks And Check Register

#### A/P Check Register

### Printing The A/P Payment Transaction Register

#### A/P Pay-G/L Trans Reg

### Reprinting All Checks

### Reprinting Selected Checks

### Voiding Payments

#### A/P Check Void Reverse Register

#### Voided Check Report

### Vouding Blank Checks

### Printing The Negative Check Report

#### A/P Vouchers Not Selected (Negatives)

#### A/P Neg. Checks Not Sel By Pay Date

### Reconciling Checks And EFT Payments

#### Selected Records Chg Back To Printed

#### Reconciled Check Report

## Working With Manual Payments

### Automatically Posting Manual Payments

#### Invoice Entry Edit List

#### A/P Invoice Transaction Register

#### A/P-G/L Trans Register

#### A/P Manual Check Register

#### A/P Pay-G/L Trans Reg

### Processing Manual Payments After Invoices Are Posted

#### A/P Manual Check Register

#### A/P Pay-G/L Trans Reg

## Working With EFT Payments

### Automatically Posting EFT Payments

#### Invoice Entry Edit List

#### A/P Invoice Transaction Register

#### A/P-G/L Trans Register

#### A/P EFT Check Register

#### A/P Pay-G/L Trans Reg

### Processing EFT Payments After Posting Invoices

#### A/P EFT Check Registe

#### A/P Pay-G/L Trans Reg

### Processing EFT Payments After Invoices Are Posted

## Working With Accounts Payable Inquiry

### Working With Invoice Voucher Inquiry

#### Displaying Invoice Detail

#### Displaying Payment Detail

### Working With Vendor Account Inquiry

### Working With Vendor Account Inquiry History

### Working With Vendor Inquiry

#### Displaying Vendor Records By Alpha Code

#### Displaying Vendor Records By Vendor Code

### Displaying Company Records

### Displaying User Profile Records

### Displaying Company A/P And G/L Options

### Displaying Period Date Records

### Displaying Calendar Records

### Displaying Period Status Records

### Displaying Bank Records

### Displaying Terms Records

### Displaying A/P Item Records

## Working With Accounts Payable Reports

### Printing A Cash Requirements Report

#### A/P Cash Requirements Report By Pay Date and Vendor

#### A/P Cash Requirements Report By Batch

### Printing A Cash Forecast Report

#### Vendor Aging Summary

#### A/P Cash Forecast Report

### Printing An Open Credits Report

#### A/P Open Credits

### Printing An Invoice Journal Report

#### A/P Invoice Journal

#### Invoice Journal By Post Date

### Printing A Payment Journal Report

#### A/P Payment Journal

#### A/P Payments By Vendor

### Printing An Invoice/Voucher List

#### A/P Payment Edit

#### A/P Payment Edit-Alpha

### Printing A Tobacco Invoice Report

#### Tobacco Invoice Report

### Printing An Outstanding Checks Report

#### A/P Outstanding Check Reconciliation

#### A/P Check Reconciliation Report (EFT's only)

#### Outstanding Chk Rpt (Excluding EFTs)

## Printing A Recurring Invoice List

### Recurring Invoice List

### Printing A Vendor History Report

#### Vendor History Report - Summary Version

#### Vendor History Report - Detail Version

### Printing A Vendor 1099 Report

#### A/P Vendor 1099 Report

### Printing Vendor Address Labels

### Printing Vendor Lists

#### Vendor List By Code

#### Vendor List By Alpha Code

#### Vendor List By Type

#### Vendor List By Amount Due

### Printing Vendor File Labels

### Printing A Bank List

#### Bank List

### Printing A Terms List

#### Vendor Terms List

### Printing An A/P Items List

#### Item List

## Working With Closing Applications

### Saving Accounts Payable Data To Tape

### Printing Accounts Payable Monthly Reports

#### Accounts Payable Monthly Report

#### Accounts Payable Monthly Report By Vendor

### Closing A Month

#### A/P Month End Close Report

## Closing A Year