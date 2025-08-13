
# Resources-App
A resources app for studying Math, Further Math, and Physics. This tool helps users organise their study schedule by subject, topic, and due date, with a user-friendly interface. Coded on Linux.

## Features

* **Task Management:** Add new study tasks with a specific subject, topic, and due date.
* **Date Selection:** Can Use a modern calendar widget to easily pick due dates without manual typing.
* **Persistent Storage:** All tasks are saved to a local JSON file (`study_planner_data.json`), so your schedule is available every time you run the application.
* **Task Status Tracking:** Mark tasks as complete and view them in a separate list.
* **Responsive UI:** The application window is resisable, and the task list uses a scrollable frame for easy navigation.

---

## Getting Started

### Prerequisites

Make sure you have **Python** installed on your system. You will also need to install the following libraries:

```sh
pip install requests
pip install tkcalendar
pip install pyinstaller
````

### Installation and Usage

1.  Clone this repository or download the project files.
2.  Make sure you have the necessary `data.json` and `study_planner.py` files.
3.  Open your terminal or command prompt in the project's directory.
4.  Run the main application file:

<!-- end list -->

```sh
python app.py
```

-----

## Creating an Executable (.exe) File

If you want to create a standalone executable for Windows or Linux that doesn't require a Python installation, follow these steps.

### On Linux

This is the recommended method for creating an executable on a Linux system.

1.  **Navigate to the project root.**
    Make sure your terminal is in the main `study app` directory.

2.  **Run PyInstaller from your virtual environment.**
    This ensures all dependencies are correctly bundled.

    ```sh
    venv/bin/python -m PyInstaller --onefile --noconsole \
    --add-data 'data.json:.' \
    --add-data 'favorites.json:.' \
    --add-data 'study_plan.json:.' \
    --add-data 'study_planner_data.json:.' \
    --add-data 'venv/lib/python3.13/site-packages/tkcalendar:tkcalendar' \
    app.py
    ```

### On Windows

1.  **Navigate to the project root.**
    Open a command prompt in the main `study app` directory.

2.  **Run PyInstaller.**
    The command for Windows uses a semicolon `;` instead of a colon `:`.

    ```sh
    pyinstaller --onefile --noconsole ^
    --add-data "data.json;." ^
    --add-data "favorites.json;." ^
    --add-data "study_plan.json;." ^
    --add-data "study_planner_data.json;." ^
    app.py
    ```

    (The `^` character is used for line continuation in Windows Command Prompt.)

### Finding the Executable

After the PyInstaller command completes successfully, your executable file will be located in the newly created `dist` folder within your project directory. You can then run it directly.

-----

## Project Structure

  * `app.py`: The main entry point for the application.
  * `study_planner.py`: Contains the core logic and GUI for the study planner.
  * `data.json`: A file containing subjects and topics for the comboboxes.
  * `study_planner_data.json`: (Generated on first run) Stores all your active and completed study tasks.

-----

## Future Possibilities

  * **Cloud Synchronisation:** Implements a backend database (like Firestore) to sync tasks across multiple devices.
  * **Notifications:** Add reminders and notifications for upcoming or overdue tasks.
  * **User Authentication:** Add user login functionality to support multiple users.
