# My Reminder App

## Overview

My Reminder App is a small Python command-line project that helps a user schedule personal reminders. The user can enter a task, choose a date and time, receive an alert when the reminder is due, and view previously saved reminders.

The project was designed as a practical application of Python functions, classes, modules, file handling, date/time processing, validation, JSON storage, and background threads.

## Features

- Add a new reminder with a task, date, and time.
- Validate the task and date/time entered by the user.
- Schedule the reminder without freezing the main menu.
- Display an alert when the reminder becomes due.
- Save reminder history in a local JSON file.
- View reminder history after restarting the program.
- Handle invalid input without terminating the application.

## Technologies Used

- Python 3
- Python standard library
- `datetime` for date and time handling
- `threading` for background reminder alerts
- `json` for local data storage
- `unittest` for testing

No external Python packages are required.

## Project Structure

```text
Reminder_VITyarthi_Project/
├── app/
│   ├── __init__.py
│   ├── menu.py
│   ├── models.py
│   ├── reminder_manager.py
│   ├── scheduler.py
│   ├── storage.py
│   └── validation.py
├── data/
│   └── reminders.json
├── docs/
│   ├── design.md
│   └── report_content.md
├── tests/
│   ├── test_storage.py
│   └── test_validation.py
├── main.py
├── statement.md
├── README.md
└── requirements.txt
```

## How to Run

1. Install Python 3.10 or later.
2. Open a terminal in the project folder.
3. Run:

```bash
python main.py
```

4. Choose an option from the menu.
5. For a reminder, enter the date in `DD-MM-YYYY` format and time in `HH:MM` format.

The application must remain open for a scheduled background alert to appear.

## Testing

Run all automated tests with:

```bash
python -m unittest discover -s tests -v
```

The tests cover date/time validation, task validation, and JSON storage.

## Design Notes

The application is intentionally split into small modules. The menu handles interaction, the manager contains the main application logic, validation handles user input, storage handles persistence, the scheduler handles background timing, and the model represents a reminder.

This makes the project easier to understand, test, and extend.

## Limitations

- Reminders are local to the computer where the program runs.
- The current version provides a terminal alert rather than a desktop/mobile notification.
- A reminder scheduled for a time while the program is closed will remain in history but will not trigger an alert during the closed period.

## Future Enhancements

- Add edit and delete reminder options.
- Add recurring reminders.
- Add desktop notifications.
- Add a graphical user interface.
- Add sorting and filtering of reminders.
- Add a small database such as SQLite.

## References

- Python documentation: https://docs.python.org/3/
- Python `datetime` documentation: https://docs.python.org/3/library/datetime.html
- Python `threading` documentation: https://docs.python.org/3/library/threading.html
- Python `unittest` documentation: https://docs.python.org/3/library/unittest.html
