# To run docker containers in development mode

- command to start building images and containers:
  sudo bash start-dev.sh

# TASK-1 FIX BUGS

- Checking the health of the entire project, including creation of contests, images of various pictures.
- Check if it works correctly: sending messages, deleting money/fee for the competition/competitions.
- General code style of the entire project (same type of database queries) and functions.

The main thing is that your code should be of the same type, in a single style (component structure, controllers,
database access, etc.) As for refactoring, this is not an end in itself, but a demonstration skills, so you can limit yourself to just rewriting
places are bad.

# TASK-2 LAYOUT

- Dynamic branding. The user wants to be always in trend and to match the season or, let's say, for the New Year, wants to update slogan, logo or name. For this, it is necessary to give the user the ability to create a timer and monitor when the time comes creating a new contest. Create a new Events page and link no. Make it possible to enter data (name of the event, date, time, for how long to notify the user about the upcoming timer) and button confirmation. Each new countdown timer the time specified by the user must be placed in list. The list of timers must be sorted (nearest event above). When the timer reaches the user-specified time - display a red badge with the number of events. Example timers - see screen. Do not forget about the component approach and adaptive. Don't forget to stop the timers when the component is unmounted. It will be a plus if the timer component is written in hooks. Data stored on the front, local storage.

- Using this page https://www.squadhelp.com/start-contest?step=2&type=1 is required to make the ButtonGroup a component.

# TASK-3 DB NO-SQL

- Need to find and count how many records are in the collection Messages contain the word "паровоз". Use aggregation for these purposes. Perform the calculation on the database side. All this for 1 request.

# TASK-4 DB SQL

- To the existing no-sql DB, you need to develop a structure databases using SQL(PostgreSQL) for chats, using an existing database as a reference. Necessary minimize consequences after server migration from no-sql to sql (e.g. column names should be the same if possible). The changes that will affect the user table, it is necessary to modify strictly via SQL(ALTER TABLE users..., etc...). results work must be uploaded to git as a separate SQL file. Provide UML diagrams as a screenshot with all possible relationships (don't forget to link the table users).

- Display the number of users by roles {admin: 40, customer: 22, ...}

- All users with the customer role who performed orders on New Year's holidays from 25.12 to 14.01, you need to credit 10% cashback from all orders in this period.

- For the creative role, you need to pay 3 users with the highest rating for $10 to their accounts.

# TASK-5 NODEJS

- Create an error logger. It is necessary to log to a file with a given generalized structure {message: “”, time: 1587410256097, code:404, stackTrace: {}}

- The task belongs to task No. 1. Every day at a certain time to copy the contents of the file and put it in a new file with a new name (for example, time stamp of the current day). In this case, the contents of the file before record must be transformed into another form {message: "some message", code: 500, time: 1587410256097}. Then clear the contents of the file from which you copied so that one could continue to write errors in it.

# TASK-6 FULLSTACK

- Moderation of proposals. Add a new Moderator role. Moderator can: see all offers, confirm the offer, reject the offer. Customer not must see every new offer until it not confirmed by the moderator. Important! Only a moderator can confirm the offer and no one else. moderator can't see nothing but offers! Creative can only see their offers and offer status. Provide a separate page that matches the styles of the entire table view application with offers that only a moderator can access. There will be a lot of offers, so pagination will be a plus. Add a moderator's solution mailing list to Creative's mailbox.

- Based on the database structure developed in the first task. The SQL DB section describes Sequelize models and migrations. Change related logic on client and server. That is, the application worked with chats on no-sql db, now should work exactly the same on sql db.
