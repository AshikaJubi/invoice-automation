# Exercise 13: Invoice Processing automation using OCR

### Reg No: 212221040020

## AIM:
To extract and save specific invoice details from a PDF using OCR in UiPath.

## Activities Required:
1. Read PDF with OCR
2. Matches
3. Excel Application Scope
4. Write Cell

## Procedure:
1. Create a new **InvoiceProcessing** project in UiPath Studio.
   
2. Add **Read PDF with OCR** activity to read the invoice PDF, set **FileName** to the PDF path, and select **Tesseract OCR** as the OCR engine.

3. Create **invoiceText** variable to store the OCR-extracted text.

4. Use **Matches** activity with **invoiceText** to extract specific data:
   - Invoice Number: `INV-\d+`
   - Date: `\d{2}/\d{2}/\d{4}`
   - Amount: `\$?\d+(,\d{3})*(\.\d{2})?`

5. Add **Excel Application Scope** and set **File Path** to save extracted data in Excel.

6. Use **Write Cell** activity to save:
   - Invoice Number in **A1**
   - Date in **A2**
   - Amount in **A3**

## Workflow:
![image](https://github.com/user-attachments/assets/d683ecf5-94f5-495f-9310-39c3b3ae6894)


## Output:
![image](https://github.com/user-attachments/assets/cf0b8cfb-e71d-41f9-b4c3-83810af4df2a)


## Result:
The invoice details are successfully extracted from PDF and saved in Excel.
