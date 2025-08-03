# WordPress-Task-Manager-Plugin-
A WordPress plugin for managing tasks and users, with role-based access for Project Managers and Team Members.

**Task Management System** is a WordPress plugin designed to manage tasks and users with role-based access. It allows Project Managers to create, edit, and delete tasks and users, while Team Members can view and update the status of their assigned tasks. All actions (task/user creation, editing, deletion, and status updates) are performed dynamically using AJAX, ensuring a seamless user experience without page refreshes.

**Features**

**User Management**:
Create, edit, and delete users with roles project_manager or team_member (Project Managers only).
Dynamic updates to the user list without page refresh.
Edit users via a modal with validation for unique usernames and emails.
Delete users with a confirmation prompt, preventing self-deletion.

Task Management:





Create tasks with title, description, assigned user, and status (Project Managers only).



Edit and delete tasks with dynamic table updates (Project Managers only).



Update task status via dropdowns with visual styling (e.g., different colors for open, pending, completed).



View all tasks ([task_all_tasks]) for Project Managers or assigned tasks ([task_my_tasks]) for Team Members.



Shortcodes:





[task_login]: Login form for Project Managers and Team Members.



[task_user_list]: Manage users (create, edit, delete) for Project Managers.



[task_create_task]: Create new tasks for Project Managers.



[task_all_tasks]: View and manage all tasks for Project Managers.



[task_my_tasks]: View and update assigned tasks for Team Members.



Dynamic and Styled Interface:





Uses Tailwind CSS for responsive, modern styling.



Status dropdowns are styled based on the selected status (e.g., status-pending, status-completed).



Success/error messages fade out after 3 seconds for a smooth UX.



Role-Based Access:





Project Managers: Full access to create, edit, and delete tasks and users.



Team Members: Can view and update the status of their assigned tasks.

Installation





Download the Plugin:





Clone the repository or download the ZIP file from GitHub:

git clone https://github.com/your-username/task-management-system.git



Alternatively, download the ZIP from the Releases page.



Upload to WordPress:





Navigate to your WordPress admin dashboard.



Go to Plugins > Add New > Upload Plugin.



Upload the task-management-system.zip file or place the task-management-system folder in wp-content/plugins/.



Activate the Task Management System plugin.



Database Setup:





The plugin automatically creates a database table (wp_tms_tasks) for tasks upon activation.



Ensure your WordPress database user has sufficient permissions to create and modify tables.



Set Up Pages:





Create the following WordPress pages and add the corresponding shortcodes:





Login Page: [task_login]



User Management Page: [task_user_list] (for Project Managers)



Create Task Page: [task_create_task] (for Project Managers)



All Tasks Page: [task_all_tasks] (for Project Managers)



My Tasks Page: [task_my_tasks] (for Team Members)



Example: Create a page named "Task Login", add [task_login] in the content, and publish.



Add Initial Project Manager:





By default, no users have the project_manager role. Assign this role manually:





Go to Users > All Users in the WordPress admin.



Edit a user and set their role to Project Manager using a role editor plugin (e.g., User Role Editor) or via the database (wp_usermeta table, wp_capabilities meta key).



Alternatively, create a new user via [task_user_list] after logging in as an admin and assigning the project_manager role.

Usage

Shortcodes





[task_login]:





Displays a login form for Project Managers and Team Members.



Redirects to [task_all_tasks] (for Project Managers) or [task_my_tasks] (for Team Members) upon successful login.



Example: Add to a page named "Task Login".



[task_user_list] (Project Managers only):





Displays a table of existing users (project_manager and team_member roles) with options to edit or delete.



Includes a form to create new users with username, email, password, and role.



Edit users via a modal; delete users with a confirmation prompt.



Example: Add to a page named "Manage Users".



[task_create_task] (Project Managers only):





Provides a form to create tasks with title, description, assigned user, and status.



Example: Add to a page named "Create Task".



[task_all_tasks] (Project Managers only):





Lists all tasks with title, description, assigned user, status, and actions (edit/delete).



Status can be updated via dropdowns with dynamic styling (e.g., green for completed).



Edit tasks via a modal; delete tasks with a confirmation prompt.



Example: Add to a page named "All Tasks".



[task_my_tasks] (Team Members and Project Managers):





Displays tasks assigned to the logged-in user with title, description, and status.



Users can update task status via dropdowns.



Example: Add to a page named "My Tasks".

Role-Based Access





Project Managers:





Access all shortcodes.



Can create, edit, and delete users and tasks.



Can view and manage all tasks.



Team Members:





Access [task_login] and [task_my_tasks].



Can view and update the status of their assigned tasks.

Styling





The plugin uses Tailwind CSS for a clean, responsive design.



Status dropdowns are styled with classes like status-open, status-pending, etc., defined in assets/css/tms-style.css. Example styles:
