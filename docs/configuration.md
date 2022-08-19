# Configuring Mode of Payment for Employees and Suppliers

[TODO: any additional configuration needed for a payment method to work (like credit card)?]

The options that show in the dropdown for `Mode of Payment` in a check run are determined by the `Mode of Payment` documents you have created in your ERPNext site. The Check Run application includes new fields in the `Supplier` and `Employee` doctypes to specify a default `Mode of Payment`. If populated, this option will automatically show in a check run for any payables owed to that party, as demonstrated in the images below.

![Detail of a supplier document for HIJ Telecom that shows the field for Supplier Default Mode of Payment filled in with "Check".](./assets/SupplierDefaultMoPDetail.png)

![Detail of a check run including an invoice for HIJ Telecom where the Mode of Payment column automatically shows "Check".](./assets/CheckRunDetailBoxAroundMoP.png)


## Supplier Configuration

The `Supplier` doctype has three new fields under the "Credit Limit" section to specify the "Default Supplier Mode of Payment", "Bank", and "Bank Account". As noted above, if there is a value for the "Supplier Default Mode of Payment", it will automatically show in the check run for any invoices for that supplier.

![Supplier doctype detail showing the Credit Limit section expanded with new fields for "Supplier Default Mode of Payment", "Bank", and "Bank Account".](./assets/ConfigSupplier.png)

The "Bank" and "Bank Account" fields are retrieved by the system to facilitate payments when the mode of payment is an electronic type.

## Employee Configuration

Similarly, the `Employee` doctype includes new "Mode of Payment", "Bank", and "Bank Account" fields in the "Salary Details" section. The "Mode of Payment" value will show in a check run, and the system uses the "Bank" and "Bank Account" values for electronic payments.

![Employee doctype detail showing the expanded Salary Details section with new fields for "Mode of Payment", "Bank", and "Bank Account".](./assets/ConfigEmployee.png)

## Mode of Payment

The Check Run application adds a new `type` field into the `Mode of Payment` doctype. The field helps the application properly process different types of payment methods.

For any existing or new `Mode of Payment` document, you can specify one of the following options:

- Cash
- Bank
- General
- Phone
- Electronic