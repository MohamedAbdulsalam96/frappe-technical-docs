Frappe is providing a user interface for easier virtualization for logging seperated in different views to fully virtualize the type of logs

# Log Types ( Desk Logs )
Logs that can be accessed through the Desk UI. These generally track operational events, but you can use their APIs to track anything from your Frappe apps. 
# Access Log
Access Log is a security feature that records all data exports made by all system users.

It is a tool for System Administrators to track which files were accessed or exported by system users. This is useful for tracking sensitive company information such as transactions or financials.

The following events generate access logs:

All forms and reports are printed.
Downloading confidential files
Exporting to XLSX/CSV files
System Managers can access the Access Log in ERPNext by using the Global Search or by going to:

    Home > Users and Permissions > Logs > Access Log
# Error Log
Error Log which is a renamed Scheduler Log. This is the default place for a software to report when something fails.
To call it, from code you can just write:

    frappe.log_error(frappe.get_traceback(), 'payment failed')

This will immediately log it into the Error Log table and can be viewed by the user or administrator.


# View Log
This is a log for each document and who viewed it just for viewing logs.
# Activity Log
Activity Logger is handling any activity related to any user on the system and its status whether (success/failed).

# Server Logs
Server logs typically contain lower level, transactional data than those accessible through Desk. Logs are now available at the site level as of Version 13. The Frappe Application generates these site logs, whereas many of the bench level log files are generated by the processes that support your Frappe environment. Logs can be found in your bench folder under:

    - ./logs
    - ./sites/{site}/logs

Only frappe.web.log and scheduler.log are logged at the site and bench levels at the time of writing. Some of the most useful files at the bench level could be:

    - bench.log
    - scheduler.log
    - worker.log

