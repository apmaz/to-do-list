# 📰 Todo List

**Todo List** is a simple Django web application for managing a list of tasks.  
The application allows you to create, edit, and delete tasks,  
mark them as completed, and organize them using thematic tags.

---

# 📦 Main Models

### Task ###

A task is an item in the todo list and contains the following fields:

- **content** — a text description of the task  
- **created_at** — date and time the task was created  
- **deadline** (optional) — the deadline for task completion  
- **is_done** — a boolean indicating whether the task is completed  
- **tags** — a list of tags associated with the task (many-to-many relationship)

### Tag ###

A tag represents the theme or category of a task and contains only one field:

- **name** — the name of the tag

A task can have multiple tags, and a tag can belong to multiple tasks.

---

# 🌐 Application Pages

### 🏠 Home Page (`127.0.0.1:8000/`) ###

The home page displays a list of all tasks with full management features:

- **Tasks are sorted: not completed → completed, from newest to oldest**  
- **All task information is displayed**

Each task includes:
- **A button "Complete" (if the task is not done) or "Undo" (if done) — toggles task status**
- **Links to edit and delete the task**
- **An "Add Task" button to create a new task**

Sidebar navigation includes:

- **Home — link to the main page**
- **Tags — link to the tag list page**

### 🏷️ Tag List Page ###

A table listing all tags:

- **Links to edit and delete each tag**
- **An "Add Tag" button to create a new tag**

---

## 🛠 Technologies

- Python 3.x  
- Django 4.x  
- SQLite (default)

---

## ⚙️ Installation

```bash
1. Clone the project

git clone https://github.com/apmaz/to-do-list.git
cd to-do-list

2. If you are using PyCharm, it might suggest automatically creating a venv and installing requirements, but if not:
python -m venv venv
venv\Scripts\activate (on Windows)
source venv/bin/activate (on macOS)
pip install -r requirements.txt

3. Run migrations
python manage.py migrate

4. Run the server
python manage.py runserver
```