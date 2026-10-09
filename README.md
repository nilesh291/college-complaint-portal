The College Complaint & Issue Tracking System (branded CampusCare) is a web
application where students can raise complaints about campus problems - such as a broken
projector, slow Wi-Fi, poor cleanliness or safety concerns - and follow the progress of each
complaint until it is resolved. College administrators get a dashboard with a summary of all
issues, can filter them by status, and update each complaint with a new status and a note that
students can read.🧑‍🎓

The project was developed because complaints in most colleges are still made verbally or on
paper, with no record, no accountability and no way for the student to know what happened
next. CampusCare makes the whole process transparent and traceable.
Technologies used: Python, Flask, MySQL with mysql-connector-python, Werkzeug
(password hashing), HTML, CSS and JavaScript.
Outcome: The system was installed, run and tested end to end. Student registration and login,
complaint submission, admin dashboard, status filtering, status updates with notes, progress
history and role-based access all worked as designed. In the test run, 3 users submitted and
managed 5 complaints that generated 5 progress updates.

Project Flow
• A student registers and logs in; the password is stored only as a hash.
• The student opens Raise Issue, fills category, priority, subject, location and description
and submits.
• The complaint is saved in MySQL with the status Pending and appears on the student's
dashboard.
• The admin logs in, sees counts by status, filters the list and opens a complaint.
• The admin changes the status and writes a note; the note is stored in the update history.
• The student opens the complaint and reads the new status and the progress history.

The complete project was run and tested for this report. The file database.sql was imported
unchanged and the Flask application was started on http://127.0.0.1:5000. Because MySQL
Server was not available in the test machine, MariaDB 10.11 (a drop-in, MySQL-compatible
server) was used. The browser actions were performed automatically with headless
Chromium. All screenshots below are real output of the running application, and the complaints
shown are sample test data

Summary
The College Complaint & Issue Tracking System (CampusCare) successfully provides a digital
channel for campus complaints. Students can raise issues in a few clicks and see exactly what
is happening to them, while administrators get one place to view, filter and update every
complaint. The project was installed, executed and tested, and all planned features worked
correctly.


How it solves the problem
Every complaint is stored permanently with its priority, status and history, so nothing is
forgotten. Students no longer have to follow up in person, and the college gets a clear picture
of how many issues are pending, in progress or resolved.

Future Scope
• Create admin accounts and department-wise staff roles from the web interface; assign
complaints to staff.
• Send e-mail or SMS notifications when the status of a complaint changes.
• Allow photo attachments, comments from students, and editing or withdrawing a complaint.
• Add search, pagination, charts and monthly reports (export to Excel / PDF) for
administrators.
• Move secrets to environment variables, add CSRF protection and deploy with a production
server such as Gunicorn.
