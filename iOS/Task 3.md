# Task 3 (6 marks):

## Synopsis:

MyNSB is an app containing a bunch of useful things that a student would want to use - for example, timetables, calendars, etcetera. The creation of these would require an in-depth knowledge of the iOS ecosystem, which is what we're going to be looking at in this task.

Your task is to create a single-page reminder app using `UITableView`, which must include these elements:

- A custom `UITableView` class, which has a cell type set to basic
- Gesture listeners for each cell: when a cell is swiped right, the reminder is removed
- A navigation bar with a button to add new reminders, which when clicked creates a pop-up asking for user text input. Once the user has entered text input in, a new `UITableViewCell` is generated with the text that the user has entered.

## Submission Method:

Submit the folder you completed your project in to the GitHub repository. Make sure that the folder works by re-downloading it and testing it out using Xcode. The folder name must contain your own name, so I can verify who did what.

## Marking Criteria:

- 2 marks for the storyboard file: 1 mark for creating all of the views, 1 mark for linking all of the views together correctly
- 1 mark for the implementation of a custom `UITableView` class
- 1 mark for gesture listeners
- 2 marks for navigation bar: 1 for implementing a custom navigation view, 1 for creating a listener for the navigation bar button