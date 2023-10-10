Budget Tracking application

---

HIEIGHER LEVEL STRUCTURE

---

1. Login (role based)
   a. admin role
   b. user role
2. user registration for user role only
3. Nav bar with dynamic menu from backend
4. Dashboard - (Role based)
   1. Admin will be able to select the user and see the dash board
   2. Admin would be able to see all the user data in the dash board by default
   3. admin would be able to mark user as favorite to see the dash bard
   4. use bar , line , pie chart graphs in dash board with live updates and with different filter types
5. create a header section and show the logedin user (profile photo,name,settings, notification).
6. Master page
   1. create dynmic Master page using slug, have image upload, file upload feature in master.
   2. validate and restrict to delete master if transaction data is present.
   3. as admin only has access to master show the number of records mapped to each master type and give provision see the records and delete all record notifying the user and give a time of ex- 7 days to remove the data or it will be soft deleted automatically from db after 7 days . schedule cron job.
   4. when the master data is changed have a history of it.
7. Have a master change data verification process for the admin.(maker, checker, approver)
8. TRANSACTION PART
   1. have a primary database postgressql and mongo db for transaction data.
   2. user and admin could be able to do CRUD depending on the master set up.
   3. user would able to upload excel to create and update data.
   4. user can download the transaction and also send the transaction in mail as attachment in excel and pdf format.
   5. have a limitaion to downlaod and upload the data which could be configurable.
   6. use elastic search to search the trasaction.

Technology to use
++++++++++++++++++++

1. react js
2. material ui
3. node js
4. express js
5. mongo db (mongoose)
6. postgress SQL
7. Elastic Search
