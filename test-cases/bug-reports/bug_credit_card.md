# Bug Report: Credit Card "Link" Button Remains Disabled with Valid Data

**Status:** Open  
**Severity:** High  
**Priority:** High  
**Environment:** Urban Routes Web App - Chrome v124.0  

### 📝 Description
In the "Payment Method" modal, after entering a valid 16-digit credit card number and a valid CVV/CVC code, clicking outside the fields or pressing 'Tab' does not trigger field validation. As a result, the "Link" (Enlazar) button remains disabled, preventing the user from completing the payment setup.

### 🔄 Steps to Reproduce
1. Open the Urban Routes application.
2. Click on the "Payment Method" (Método de Pago) field.
3. Click on "Add Card" (Añadir Tarjeta).
4. Enter a valid 16-digit card number (e.g., `1234 5678 1234 5678`).
5. Enter a valid 3-digit CVV code (e.g., `123`).
6. Click anywhere outside the input fields to lose focus.

### ❌ Actual Result
The input validation is not evaluated on focus loss. The "Link" button remains greyed out and unclickable despite having complete, valid payment credentials.

###  Expected Result
The application should validate the input fields upon losing focus (blur event) or dynamically as the user types. Since data matches the requirements, the "Link" button must become active and green.

### 📷 Visual Evidence
*(Placeholder for screenshot: In your real repository, you can add an image here showing the disabled button)*
