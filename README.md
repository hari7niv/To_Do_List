# Ex03 To-Do List using JavaScript
## Date: 27-3-2026

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
### index.html

```

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>To-Do List</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>To Do List</h1>
        <div class="input-area">
            <input type="text" id="taskInput" placeholder="Enter a task">
            <button id="addTask">Add Task</button>
        </div>
        <ul class="task-list" id="taskList">
        </ul>
    </div>
    <script src="script.js"></script>
</body>
</html>

```
### style.css

```

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, sans-serif;
    background: #f2f2f2;
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
}

.container {
    width: 320px;
    background: #ffffff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

h1 {
    text-align: center;
    margin-bottom: 16px;
    color: #333333;
}

.input-area {
    display: flex;
    gap: 8px;
    margin-bottom: 14px;
}

.input-area input {
    flex: 1;
    padding: 10px;
    border: 1px solid #cccccc;
    border-radius: 4px;
}

.input-area button {
    padding: 10px 14px;
    border: none;
    border-radius: 4px;
    background: #2e8b57;
    color: #ffffff;
    cursor: pointer;
}

.input-area button:hover {
    background: #256f46;
}

.task-list {
    list-style: none;
}

.task-list li {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px 0;
    border-bottom: 1px solid #eeeeee;
}

.task-list li:last-child {
    border-bottom: none;
}

.task-list li span {
    margin-right: 10px;
    color: #333333;
}

.task-list li button {
    padding: 6px 10px;
    border: none;
    border-radius: 4px;
    background: #d9534f;
    color: #ffffff;
    cursor: pointer;
}

.task-list li button:hover {
    background: #bf3f3b;
}

```
### script.js
```

document.addEventListener('DOMContentLoaded', function() {
    const taskInput = document.getElementById('taskInput');
    const addTaskButton = document.getElementById('addTask');
    const taskList = document.getElementById('taskList');
    addTaskButton.addEventListener('click', function() {
        const taskText = taskInput.value.trim();
        if (taskText !== '') {
            addTask(taskText);
            taskInput.value = ''; // Clear input after adding task
        }
    });
        taskInput.addEventListener('keypress', function(e) {
         if (e.key === 'Enter') {
            addTaskButton.click();
        }
    });
    function addTask(taskText) {
        const listItem = document.createElement('li');
        listItem.innerHTML = `
            <span>${taskText}</span>
            <button class="delete-btn">X</button>
        `;
        taskList.appendChild(listItem);
        const deleteButton = listItem.querySelector('.delete-btn');
        deleteButton.addEventListener('click', function() {
            listItem.remove();
        });
    }
});

```
## OUTPUT

<img width="1856" height="1033" alt="image" src="https://github.com/user-attachments/assets/b7467fb5-342e-42d4-b7c8-dd59799dbf72" />


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
