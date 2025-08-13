# Resources-App
A resources app for studying Math, Further Math, and Physics. This tool helps users organise their study schedule by subject, topic, and due date, with a user-friendly interface. Coded on Linux.

## Features

* **Task Management:** Add new study tasks with a specific subject, topic, and due date.
* **Date Selection:** Can Use a modern calendar widget to easily pick due dates without manual typing.
* **Persistent Storage:** All tasks are saved to a local JSON file (`study_planner_data.json`), so your schedule is available every time you run the application.
* **Task Status Tracking:** Mark tasks as complete and view them in a separate list.
* **Responsive UI:** The application window is resizable, and the task list uses a scrollable frame for easy navigation.

---

## Getting Started

### Prerequisites

Make sure you have Python installed on your system. You will also need to install the following libraries:

```sh
pip install requests
pip install tkcalendar
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

## Project Structure

  * `app.py`: The main entry point for the application.
  * `study_planner.py`: Contains the core logic and GUI for the study planner.
  * `data.json`: A dummy file containing subjects and topics for the comboboxes.
  * `study_planner_data.json`: (Generated on first run) Stores all your active and completed study tasks.

-----

## Future Possibilities

  * **Cloud Synchronisation:** Implements a backend database (like Firestore) to sync tasks across multiple devices.
  * **Notifications:** Add reminders and notifications for upcoming or overdue tasks.
  * **User Authentication:** Add user login functionality to support multiple users.

<!-- end list -->
