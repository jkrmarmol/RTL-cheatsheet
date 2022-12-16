# **@testing-library/user-event**
&nbsp;&nbsp;&nbsp;&nbsp;- is a library that provides utility functions for simulating user events in tests. It can be used in conjunction with `@testing-library/react` to test the behavior of a React component when a user interacts with it.

To use `@testing-library/user-event` with `@testing-library/react`, you will need to install both libraries and then import the functions that you want to use in your tests.

`@testing-library/user-event` provides a number of utility functions for simulating different types of user events. Here is a list of some of the commonly used `fireEvent` methods in `@testing-library/user-event`:

- `fireEvent.click(element)`: Simulates a mouse click on the specified element.
- `fireEvent.dblClick(element)`: Simulates a mouse double-click on the specified element.
- `fireEvent.change(element, eventInit)`: Simulates a change event on the specified element. The eventInit object should contain any properties that you want to set on the simulated event, such as target.value.
- `fireEvent.focus(element)`: Simulates a focus event on the specified element.
- `fireEvent.blur(element)`: Simulates a blur event on the specified element.
- `fireEvent.keyDown(element, eventInit)`: Simulates a key down event on the specified element. The eventInit object should contain any properties that you want to set on the simulated event, such as key or keyCode.
- `fireEvent.keyUp(element, eventInit)`: Simulates a key up event on the specified element. The eventInit object should contain any properties that you want to set on the simulated event, such as key or keyCode.
- `fireEvent.input(element, eventInit)`: Simulates an input event on the specified element. The eventInit object should contain any properties that you want to set on the simulated event, such as target.value.

Here is an example of how you might use some of these methods in a test:

```js
import { render, screen } from '@testing-library/react';
import { fireEvent } from '@testing-library/user-event';
import MyForm from './MyForm';

test('MyForm handles input and submit correctly', () => {
  render(<MyForm />);
  const input = screen.getByLabelText('Name');
  const button = screen.getByText('Submit');
  fireEvent.change(input, { target: { value: 'John Smith' } });
  expect(input.value).toBe('John Smith');
  fireEvent.click(button);
  // Make assertions about the form submission here
});

```

In this example, the test uses the `render` function from `@testing-library/react` to render the `MyForm` component. It then uses the `screen.getByLabelText` and `screen.getByText `methods to find the input field and submit button.

Next, the test uses the `fireEvent.change` function to simulate a change event on the input field. It then makes an assertion that the value of the input field is correct. Finally, the test uses the `fireEvent.click` function to simulate a click on the submit button.