# Interactive Slot Timetable

A lightweight, single-file web application to visualize and manage a university slot-based course timetable. Built with a dark mode aesthetic, this tool helps students track their schedule, handle overlapping slots, and persist their data locally without needing a backend server.

## Features

* **Dark Mode Interface:** A sleek, high-contrast UI designed to be easy on the eyes while ensuring course text remains legible regardless of the block color.
* **Dynamic Layout:** Automatically calculates and positions course blocks based on start and end times. If multiple courses are assigned to the same time slot, they neatly share the horizontal space side-by-side.
* **Persistent Storage:** Utilizes your browser's `localStorage`. Your timetable is automatically saved and will still be there even if you refresh the page or close your browser.
* **Interactive Color Picker:** Choose custom colors for each course. The input fields automatically tint to match your selected color, giving you real-time visual feedback before adding the course.
* **Details Modal:** Clicking on any course block opens a pop-up modal displaying the full course name and its assigned slot. 
* **Keyboard Accessibility:** The modal can be closed quickly by pressing the `Escape` key.
* **Space-Saving UI:** Long course names are automatically truncated with an ellipsis (...) to prevent layout breaking, and deleting a course is handled via a compact "✕" button.

## How to Run

This project requires zero setup, dependencies, or servers. 

1. Download or clone the repository.
2. Double-click the `timetable.html` file to open it in any modern web browser (Chrome, Firefox, Safari, Edge, etc.).

## How to Use

1. **Add a Course:**
   * Enter the course code (e.g., "CS101") in the text field.
   * Select the designated slot (e.g., "Slot 1", "Lab L1") from the dropdown menu.
   * Pick a color using the color picker to easily identify the course on the calendar.
   * Click **Add Course**.
2. **View Course Details:** * Click anywhere on a colored course block on the timetable to open a modal with its full details.
3. **Drop a Course:** * Click the small **✕** in the top right corner of the course block to remove it from your schedule.
4. **Clear Schedule:** * Click the red **Clear All** button to completely reset your timetable. (You will be prompted to confirm this action).

## Technologies Used

* **HTML5:** For the core structure and inputs.
* **CSS3:** For styling, flexbox layouts, CSS grids, custom scrollbars, and dark mode UI variables.
* **Vanilla JavaScript (ES6):** For DOM manipulation, calculating slot overlaps, handling the modal logic, and interacting with the `localStorage` API.

## Slot Mapping Reference

The application uses a pre-defined mapping system to place courses at specific times. The slots generally follow this pattern:
* Standard Morning Slots (1-3): 55 minutes each.
* Extended Morning Slots (4-7): 1 hour 25 minutes each.
* Afternoon Slots (8-11): 1 hour 25 minutes each.
* Evening Slots (12): 55 minutes.
* Labs (L1-L6): Extended ~3 hour blocks.
* Miscellaneous (X slots): Used for varied 55-minute blocks.
