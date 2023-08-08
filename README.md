# Frappe Actions

Frappe Actions is a Python library that allows you to perform various actions on Frappe Framework, such as creating documents, updating fields, sending emails, or triggering workflows.

## Installation

To install Frappe Actions, you need to have Frappe Framework installed on your system. You can follow the official guide [here](https://frappeframework.com/docs/user/en/installation).

Then, you can use pip to install Frappe Actions:

```bash
pip install frappe-actions
```

## Usage

To use Frappe Actions, you need to import the library and create an instance of the `FrappeActions` class with your Frappe site URL and API key and secret. For example:

```python
from frappe_actions import FrappeActions

fa = FrappeActions("https://example.com", "your_api_key", "your_api_secret")
```

Then, you can use the methods of the `FrappeActions` class to perform various actions on Frappe. For example:

```python
# Create a new document of type "ToDo"
todo = fa.create_doc("ToDo", {"description": "Test Frappe Actions"})

# Update a field of an existing document
fa.update_doc("ToDo", todo["name"], {"status": "Closed"})

# Send an email to a recipient
fa.send_email("test@example.com", "Hello from Frappe Actions", "This is a test email")

# Trigger a workflow action on a document
fa.trigger_workflow("Sales Order", "SO-0001", "Approve")
```

For more details and examples, please refer to the [documentation](https://frappe-actions.readthedocs.io/en/latest/).

## Contributing

Frappe Actions is an open source project and welcomes contributions from anyone who is interested in improving it. If you want to contribute, please follow these steps:

- Fork the repository on GitHub and clone it to your local machine.
- Create a new branch for your feature or bug fix.
- Write your code and test it with pytest.
- Push your changes to your fork and create a pull request on GitHub.
- Wait for the maintainers to review and merge your pull request.

If you have any questions or suggestions, please feel free to open an issue or contact the author at puneeth5127@gmail.com

## License

Frappe Actions is licensed under the MIT License. See the [LICENSE](https://github.com/puneethkotha/frappe_actions/blob/master/license) file for more details.
