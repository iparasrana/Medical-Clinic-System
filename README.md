# Medical Clinic System

## Phase 1: Command-Line Interface (CLI)

### Setup
Run the CLI by executing the following command:
```bash
python3 -m clinic cli
```

### Interact with the System
1. Log in to the application.
2. Perform the following operations:
   - Create, update, retrieve, and delete patients.
   - Create and manipulate notes.
3. Observe how the system handles user inputs and updates the data.

### Code Analysis
- Understand how the CLI interacts with the controller and model.
- Observe patterns for error handling (e.g., `try-except` blocks or `if` checks).
- Note the separation between:
  - **Data Manipulation**: Handled by the controller and model.
  - **User Interaction**: Handled by the view.

## Phase 2: Graphical User Interface (GUI)

### Initial Setup
1. Install PyQt6 using pip:
   ```bash
   pip install PyQt6
   ```
2. Ensure the `clinic/gui` directory contains `clinic_gui.py` as the main entry point for your GUI.
3. Run the GUI using:
   ```bash
   python3 -m clinic gui
   ```

### Design Guidelines
The GUI follows the **Model-View-Controller (MVC)** pattern:
- **Model**: Represents the application's data (e.g., patients, notes).
- **View**: Handles the GUI (PyQt6 windows, widgets).
- **Controller**: Acts as an intermediary between the view and model.

#### Modular Components
- Use separate PyQt6 widgets for different functionalities, such as patient management and note management.

### Functional Requirements
- Implement the following user stories:
  - Log in/out.
  - Create, update, delete, and retrieve patients/notes.
- Use appropriate PyQt6 widgets:
  - **QTableView**: For listing and retrieving patients.
  - **QPlainTextEdit**: For listing and retrieving notes.
- Test GUI interactions to ensure smooth functionality.

### Best Practices
#### Development
- Develop incrementally:
  - Start with simple functionalities (e.g., log in/log out).
  - Progress to more complex ones (e.g., patient and note management).
- Use error handling to ensure a smooth user experience.

#### Usability
- Provide clear labels, buttons, and messages.
- Validate inputs before processing.
- Display meaningful error messages for invalid inputs.

#### Documentation and Version Control
- Document all major changes and features.
- Use version control (e.g., Git) to track updates.

## Improvements

### Database Integration
- Transition from file-based storage to a robust database solution:
  - Use **SQLite** for lightweight and portable database needs.
  - Optionally integrate **MySQL** for more complex or scalable requirements.
- Update the codebase to interact with the database using a well-defined schema.

### Enhanced User Experience (UX)
- Redesign the user interface for simplicity and ease of use.
- Implement responsive design for compatibility across devices and screen sizes.
- Incorporate intuitive navigation and meaningful feedback for user actions.
- Use modern UI/UX frameworks or libraries for a polished appearance.

### Form Validation
- Ensure all user inputs are validated:
  - Validate on both client and server sides.
  - Provide clear error messages for invalid inputs.
  - Use regex and libraries to validate specific fields (e.g., email, phone numbers).
- Prevent SQL injection and other vulnerabilities during input handling.

### Convert into Standalone Installable Software
- Package the application as a standalone executable using tools like:
  - **PyInstaller**
  - **Electron**
  - Native OS-specific methods.
- Ensure easy installation across multiple operating systems (Windows, macOS, Linux).
- Include an installer wizard for guided installation.
- Provide offline functionality with a bundled local database.

## Features
- User-friendly interface.
- Scalable with database integration.

## Installation
1. Download the zip file.
2. Extract the contents.
3. Run the `clinic_gui` executable in the `dist` folder.
4. Use the following credentials to log in:
   - **Username**: `user`
   - **Password**: `123456`
5. Follow the on-screen instructions.

---

Developed with care to streamline medical clinic management and improve user experience.
