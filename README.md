  WordPress Report Processing Script
  Note: This script is specifically designed to process .xls reports generated by a specific company using a WordPress-based system. The input file structure must match the expected format for the script to work correctly. Using files with a different structure will likely cause errors.
  
  Overview
  This script automates the processing of customer order data exported from a WordPress system. The raw report includes repetitive customer information for each product they ordered. For instance, if a customer orders three products, their data is repeated across three rows. The script cleans and processes this data, turning it into a more readable and actionable format suitable for analysis and logistics.
  
  What the script does:
  Handles duplicate customer data:
  
  Consolidates repetitive customer information into a single entry.
  Cleans raw data:
  
  Removes redundant HTML tags (e.g., <i>, <b>) in product names that result from website styling.
  Processes product bundles:
  
  Breaks down predefined product bundles (e.g., Pakiet Klasyczny) into individual items with their respective quantities.
  Calculates product weights:
  
  Converts product quantities into total weight in kilograms (e.g., 150g, 500g, and 1kg products are aggregated into kilograms).
  Generates reports for logistics:
  
  Filters out unnecessary data to create a delivery report for the courier service, containing only the relevant information.
  Formats Excel sheets:
  
  Automatically adjusts column widths, highlights important rows (e.g., "w kawałku"), and organizes the data into three separate sheets.
  
  Input Data
  The script works exclusively with .xls reports generated by a company using a WordPress system. The file must contain the following key columns:
  
  'Line number'
  'Email (Billing)'
  'First Name (Shipping)'
  'Last Name (Shipping)'
  'Address 1&2 (Shipping)'
  'City (Shipping)'
  'Postcode (Shipping)'
  'Order Subtotal Amount'
  'Order Shipping Amount'
  'Item Name'
  'Quantity (-Refund)'
  'SKU'
  'Item #'
  
  Products (Produkty):
  
  A consolidated list of all products, including unpacked product bundles with summed quantities.
  Cleaned product names (HTML tags removed).
  Product Weights (Produkty Gramatury):
  
  A summary of product weights aggregated in kilograms.
  Couriers (Kurierzy):
  
  A logistics-friendly report containing only relevant delivery information, such as customer address and order details.
