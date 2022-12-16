# **@testing-library/react**

&nbsp;&nbsp;&nbsp;&nbsp;- is a library that provides utility functions for testing React components. One of the commonly used methods in this library is screen. The screen method is a helper function that allows you to access the rendered elements in the DOM. You can use it to select elements from the DOM and make assertions about their content or state.
 

## **Here is a list of some of the commonly used `.screen` method :**

### **screen.getBy**
- `screen.getByText(text)`: Finds an element that contains the specified text.
- `screen.getByLabelText(text)`: Finds an element with a label attribute whose value contains the specified text.
- `screen.getByPlaceholderText(text)`: Finds an element with a placeholder attribute whose value contains the specified text.
- `screen.getByAltText(text)`: Finds an element with an alt attribute whose value contains the specified text.
- `screen.getByTitle(text)`: Finds an element with a title attribute whose value contains the specified text.
- `screen.getByTestId(id)`: Finds an element with a data-testid attribute whose value contains the specified text.
- `screen.getByRole(role)`: Finds an element with a role attribute whose value contains the specified text.

These methods return the first element that matches the specified criteria. If no matching element is found, they will throw an error.


### **screen.query**
- `screen.queryByText(text)`: Finds an element that contains the specified text.
- `screen.queryByLabelText(text)`: Finds an element with a label attribute whose value contains the specified text.
-`screen.queryByPlaceholderText(text)`: Finds an element with a placeholder attribute whose value contains the specified text.
- `screen.queryByAltText(text)`: Finds an element with an alt attribute whose value contains the specified text.
- `screen.queryByTitle(text)`: Finds an element with a title attribute whose value contains the specified text.
- `screen.queryByTestId(id)`: Finds an element with a data-testid attribute whose value contains the specified text.
- `screen.queryByRole(role)`: Finds an element with a role attribute whose value contains the specified text.

These methods return the first element that matches the specified criteria, or `null` if no matching element is found.

### **screen.find**
- `screen.findByText(text)`: Finds an element that contains the specified text.
- `screen.findByLabelText(text)`: Finds an element with a label attribute whose value contains the specified text.
- `screen.findByPlaceholderText(text)`: Finds an element with a placeholder attribute whose value contains the specified text.
- `screen.findByAltText(text)`: Finds an element with an alt attribute whose value contains the specified text.
- `screen.findByTitle(text)`: Finds an element with a title attribute whose value contains the specified text.
- `screen.findByTestId(id)`: Finds an element with a data-testid attribute whose value contains the specified text.
- `screen.findByRole(role)`: Finds an element with a role attribute whose value contains the specified text.

These methods return a `Promise` that resolves to the first element that matches the specified criteria. If no matching element is found, the `Promise` will be rejected with an error.