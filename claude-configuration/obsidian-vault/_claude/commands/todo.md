# Task manager for Obsidian
This command helps you create and mark as complete tasks in Obsidian. 

## Task format

### Pending task
- [ ] #task <Task description> [#when/this_week] [priority] [recurrence] creation_date [due_date]

### Completed task
- [x] #task <Task description> [#when/this_week] [priority] [recurrence] creation_date [due_date] completed_date

### Fields
- The ones in brackets are optional. Only add them if you have the information.
- 'priority' can be 'l'/'low' ⏬ or 'h'/high 🔺. Format: ⏬ (for low) or 🔺 (for high)
- 'creation_date' is the date the task was created. Format: ➕ YYYY-MM-DD
- 'due_date' is the date the task is due. Format: 📅 YYYY-MM-DD
- 'completed_date' is the date the task was completed. Format: ✅ YYYY-MM-DD
- 'recurrence' is the recurrence of the task. The <recurrence description> is plain text. Format: 🔁 <recurrence description>

## Create a task
If the location is not 
specified, append it to a file in the '0 INBOX' folder of the Obsidian vault that follows
the format YYYY-MM-DD Capture.md. If the file does not exist, create it. If the location is specified, append it to the 'Plan', 'One offs', or 'Tasks' section if it exists, in that order. Only search for locations within the '0 INBOX', '1 PROJECTS', AND '2 AREAS' folders and subfolders.

If added to the INBOX, you should indicate the time it was created in the line before if it is not 
already there, with the format:
**HH:MM:**

## Mark a task as complete
1. With the available information, find the task in the INBOX or in the corresponding project or area main note that matches best the description.
2. Mark the task as complete, adding the completed_date field with the current date, and adding the 'x' to the checkbox.

## List tasks
1. Identify the search critera from the available information (like project or due date).
2. Search for the tasks in the corresponding folders (e.g. '1 PROJECTS', '2 AREAS', '0 INBOX' if there is no project or area specified, otherwise only in the project or area subtree).
3. Show a list of the tasks that match the search criteria sorted by due date.
If there is no due date, show only the ones with due date within this week or overdue (the ones marked with #when/this_week would fulfil the criteria). The tasks you show must have a due date or a #when/this_week tag.

Usage:
'/todo add Task description' - Add a task to the capture file in the INBOX.
'/todo add [options] <-m|--message> Task description' - Add a task to the corresponding project or area main note. The project area or name may not match 100%.
'/todo complete Task description' - Mark a task as complete.

The following options are available:
'-p, --project Project name' - Specifies the project or area to add the task to its main note. The project area or name may not match 100%.
'-m, --message Task description' - Specifies the task description.
'-d, --due Due date' - Specifies the due date of the task. The format is YYYY-MM-DD.
'-P, --priority Priority' - Specifies the priority of the task. It can be 'l'/'low' ⏬ or 'h'/high 🔺.
