# AnnaPay
Solution Approach: Our solution was to create a centralized notification system within the payroll module. This system sends automated reminders and alerts to all stakeholders, including employees, managers, and HR/employers, based on payroll events.
     How the System Works 
   We created two types of notifications:  
   1) Scheduled Notifications  
     (Example: Timesheet deadline reminder)  
   2)Event-Based Notifications  
     (Example: Salary credited, payroll approved, payroll failure)

Notifications
Employee Notifications:
  1)Timesheet deadline approaching
  2)Final reminder on deadline day
  3)Payslip generated
  4)Salary credited
  5)Missing bank details
Example:
            1)If timesheet not submitted AND deadline is tomorrow then Send SMS
2)If salary processed then Notify employee
        Manager Notifications:
        1)Team members have pending timesheets
        2)Payroll ready for approval
        3)Payroll approval pending
      Example:
1)If payroll requires approval then Notify manager
      Employer Notifications:
       1)Payroll processing started.
       2)Payroll processing completed 
       3)Payroll failure or error
       4)Bank transfer file generated
    Example 
1)	If payroll is completed, notify HR. 
    Technical Design: Notification Flow After CSV Upload
    Step 1: HR Uploads Salary CSV File
    1)HR uploads the salary details file.
    2)System validates the file format and required fields.
    If Upload is Successful:
    1)Payroll status → **Processing**
     2)HR receives notification:
    * Then Salary file uploaded successfully. Payroll processing has started.”
    *This indicates that the system has accepted the file.
  Step 2: Payroll Processing Begins
* System begins salary calculations.
* Data validation occurs in the background.
 During Processing:
If Validation Error Found:
1) Payroll status → **Validation Failed**
2)HR receives notification:
Then Payroll file validation failed. Please review and re-upload.”
If Employee Bank Details Missing:
1)That particular employee receives notification stating that
Your bank details are missing. Please update to avoid salary delay.
2)This prevents HR from manually checking and avoids delays.
Step 3: Payroll Completed Successfully
1)Payroll status them Completed
   *Notifications Sent:
   *Employees receive:
    *Your salary for [Month] has been credited
  HR receives:
  Payroll processing completed successfully

Step 4: Payroll Failure 
Payroll status → Failed
Notification Sent:
HR receives critical alert:
Payroll processing failed. Immediate action required
*This allows quick corrective action.
and takes the necessary needed action

Future Scope :
1)Using Ai can help to spot salary mistakes, warn about wrong cuts, guess problems before they happen, and give tips to save tax.
2)Different people get different alerts: HR, bosses, workers, or whole teams.
3)It will remind about tax laws, PF payments, audits, and year-end work to stay legal







