**SNEasyScheduledJob**
======================

This is a low code ServiceNow app aimed at admins to help them schedule jobs using UI.

**Description:**
----------------

ServiceNow platform is moving towards no-code or low-code direction but, there is still no out of the box way a system admin can schedule a job for processing some records without scripts. This app is aimed at bridging the gap and allow a system admin to copy, update or delete records, all by configuring options from UI.

**Installation:**
-----------------

*Install the updateset found in dist folder* - "Easy Scheduled Job-V1" updateset creates the application and all the needed components in the instance. All the components that are being created are new and do not change any out of the box settings.

**Usage:**
----------

Once you have installed the application, you can access this from the left navigation as 'Easy Scheduled Job' application. Use 'New' menu to create new job and 'All' to view all the jobs created. Use 'Log' menu to view logs related to this application. Guided tour is added instead of static documentation.

![Application](https://github.com/iamkalai/SNEasyScheduledJob/blob/master/doc/images/Menu.png)


**Current Design Restrictions:**
--------------------------------

- Extended sysauto_script table instead of modifying so that we do not touch or modify anything out of the box.
- The record filter is made mandatory so that people would not incorrectly run the job against the entire table. Admin should take consious decision if they want to process the entire table.
- Description field is added so that the jobs have on-platform documentation stating its purpose.
- For delete action, run workflow option is not provided because people may end up deleting the parent records without taking care of child records.


**License:**
------------
GNU General Public License v3.0
