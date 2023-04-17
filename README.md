# NIM-Conn-System-REST-Google-Workspace


This is a native rest connector. This repo is for additional tools specific to Google Workspace

## Table of Contents
* [Getting Started](#getting-started)
* [Automated Deletion](#automated-deletion)  

## Authorization Scopes
|Table                                     |Read                                                                                                                                                                                                                                                                                  |CUD                                                                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|chromeosdevices                           |https://www.googleapis.com/auth/admin.directory.device.chromeos                                                                                                                                                                                                                       |https://www.googleapis.com/auth/admin.directory.device.chromeos                                                                                                                                                        |
|classroom_courses                         |https://www.googleapis.com/auth/classroom.courses                                                                                                                                                                                                                                     |https://www.googleapis.com/auth/classroom.courses                                                                                                                                                                      |
|classroom_course_aliases                  |https://www.googleapis.com/auth/classroom.courses                                                                                                                                                                                                                                     |https://www.googleapis.com/auth/classroom.courses                                                                                                                                                                      |
|classroom_course_students                 |https://www.googleapis.com/auth/classroom.courses,https://www.googleapis.com/auth/classroom.rosters,https://www.googleapis.com/auth/classroom.profile.emails,https://www.googleapis.com/auth/classroom.profile.photos,https://www.googleapis.com/auth/classroom.guardianlinks.students|https://www.googleapis.com/auth/classroom.rosters                                                                                                                                                                      |
|classroom_course_teachers                 |https://www.googleapis.com/auth/classroom.rosters                                                                                                                                                                                                                                     |https://www.googleapis.com/auth/classroom.rosters                                                                                                                                                                      |
|classroom_invitations                     |https://www.googleapis.com/auth/classroom.rosters                                                                                                                                                                                                                                     |https://www.googleapis.com/auth/classroom.rosters                                                                                                                                                                      |
|classroom_userProfiles_guardianInvitations|https://www.googleapis.com/auth/classroom.guardianlinks.students                                                                                                                                                                                                                      |https://www.googleapis.com/auth/classroom.guardianlinks.students                                                                                                                                                       |
|classroom_userProfiles_guardians          |https://www.googleapis.com/auth/classroom.guardianlinks.students                                                                                                                                                                                                                      |https://www.googleapis.com/auth/classroom.guardianlinks.students                                                                                                                                                       |
|datatransfer_transfers                    |https://www.googleapis.com/auth/admin.datatransfer                                                                                                                                                                                                                                    |https://www.googleapis.com/auth/admin.datatransfer                                                                                                                                                                     |
|drive_drives                              |https://www.googleapis.com/auth/drive                                                                                                                                                                                                                                                 |https://www.googleapis.com/auth/drive                                                                                                                                                                                  |
|groups                                    |https://www.googleapis.com/auth/admin.directory.group                                                                                                                                                                                                                                 |https://www.googleapis.com/auth/admin.directory.group                                                                                                                                                                  |
|groups_aliases                            |https://www.googleapis.com/auth/admin.directory.group                                                                                                                                                                                                                                 |https://www.googleapis.com/auth/admin.directory.group                                                                                                                                                                  |
|groups_settings                           |https://www.googleapis.com/auth/apps.groups.settings                                                                                                                                                                                                                                  |https://www.googleapis.com/auth/apps.groups.settings                                                                                                                                                                   |
|licenses                                  |                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                       |
|license_assignments                       |https://www.googleapis.com/auth/apps.licensing                                                                                                                                                                                                                                        |https://www.googleapis.com/auth/apps.licensing                                                                                                                                                                         |
|members                                   |https://www.googleapis.com/auth/admin.directory.group                                                                                                                                                                                                                                 |https://www.googleapis.com/auth/admin.directory.group                                                                                                                                                                  |
|mobiledevices                             |https://www.googleapis.com/auth/admin.directory.device.mobile                                                                                                                                                                                                                         |https://www.googleapis.com/auth/admin.directory.device.mobile                                                                                                                                                          |
|orgunits                                  |https://www.googleapis.com/auth/admin.directory.orgunit                                                                                                                                                                                                                               |https://www.googleapis.com/auth/admin.directory.orgunit                                                                                                                                                                |
|privileges                                |https://www.googleapis.com/auth/admin.directory.rolemanagement                                                                                                                                                                                                                        |                                                                                                                                                                                                                       |
|roleAssignments                           |https://www.googleapis.com/auth/admin.directory.rolemanagement                                                                                                                                                                                                                        |https://www.googleapis.com/auth/admin.directory.rolemanagement                                                                                                                                                         |
|roles                                     |https://www.googleapis.com/auth/admin.directory.rolemanagement                                                                                                                                                                                                                        |                                                                                                                                                                                                                       |
|users                                     |https://www.googleapis.com/auth/admin.directory.user                                                                                                                                                                                                                                  |https://www.googleapis.com/auth/admin.directory.user,https://www.googleapis.com/auth/admin.directory.user.security,https://www.googleapis.com/auth/admin.directory.user                                                |
|users_aliases                             |https://www.googleapis.com/auth/admin.directory.user                                                                                                                                                                                                                                  |https://www.googleapis.com/auth/admin.directory.user                                                                                                                                                                   |
|users_asps                                |https://www.googleapis.com/auth/admin.directory.user.security                                                                                                                                                                                                                         |https://www.googleapis.com/auth/admin.directory.user.security                                                                                                                                                          |
|users_gmail_settings_autoforwarding       |https://www.googleapis.com/auth/gmail.settings.basic                                                                                                                                                                                                                                  |https://www.googleapis.com/auth/gmail.settings.sharing                                                                                                                                                                 |
|users_gmail_settings_delegates            |https://www.googleapis.com/auth/gmail.settings.basic                                                                                                                                                                                                                                  |https://www.googleapis.com/auth/gmail.settings.sharing                                                                                                                                                                 |
|users_gmail_settings_forwardingAddresses  |https://www.googleapis.com/auth/gmail.settings.basic                                                                                                                                                                                                                                  |https://www.googleapis.com/auth/gmail.settings.basic,https://www.googleapis.com/auth/gmail.settings.sharing,https://www.googleapis.com/auth/gmail.settings.basic,https://www.googleapis.com/auth/gmail.settings.sharing|
|users_gmail_settings_imap                 |https://www.googleapis.com/auth/gmail.settings.basic                                                                                                                                                                                                                                  |https://www.googleapis.com/auth/gmail.settings.basic                                                                                                                                                                   |
|users_gmail_settings_language             |https://www.googleapis.com/auth/gmail.settings.basic                                                                                                                                                                                                                                  |https://www.googleapis.com/auth/gmail.settings.basic                                                                                                                                                                   |
|users_gmail_settings_pop                  |https://www.googleapis.com/auth/gmail.settings.basic                                                                                                                                                                                                                                  |https://www.googleapis.com/auth/gmail.settings.basic                                                                                                                                                                   |
|users_gmail_settings_sendas               |https://www.googleapis.com/auth/gmail.settings.basic                                                                                                                                                                                                                                  |https://www.googleapis.com/auth/gmail.settings.basic                                                                                                                                                                   |
|users_gmail_settings_vacation             |https://www.googleapis.com/auth/gmail.settings.basic                                                                                                                                                                                                                                  |https://www.googleapis.com/auth/gmail.settings.basic                                                                                                                                                                   |
|users_tokens                              |https://www.googleapis.com/auth/admin.directory.user.security                                                                                                                                                                                                                         |https://www.googleapis.com/auth/admin.directory.user.security                                                                                                                                                          |
|users_verificationCodes                   |https://www.googleapis.com/auth/admin.directory.user.security                                                                                                                                                                                                                         |https://www.googleapis.com/auth/admin.directory.user.security                                                                                                                                                          |



## Available Provisioning Actions
* Create user account 
* Enable user account
* Disable user account
* Delete user account
* Group Membership (Add / Remove)



## Custom Schemas
If you need to import custom schema data into NIM you can extend the table schemas by adding a custom json file. 

C:\ProgramData\Tools4ever\NIM\config\rest\systems\SYSTEMNAME.json

SYSTEMNAME = The name of the system in NIM.

A a sample file (CustomSchema.json) is provide in this repo.

## Automated Deletion

### Custom Schema Fields
![image](https://user-images.githubusercontent.com/24281600/135354425-b5cd03e1-8fb9-43a8-9542-5c8d801c827f.png)


### Example Filter
![image](https://user-images.githubusercontent.com/24281600/135354511-235f5dea-0b52-4706-865e-25c691700292.png)


### Populate Automated Deletion Date
This script column sets up the automated deletion date so it can be populated in AD when the account is disabled
```
let daysInFuture = 365;

let date = new Date();
date.setDate(date.getDate() + daysInFuture);
let year = date.getUTCFullYear();
let month = date.getUTCMonth()+1;
let day = date.getUTCDate();

if (day < 10) { day = '0' + day; }
if (month < 10) { month = '0' + month; }

let deleteDate = '' + year + '-' + month + '-' + day

return deleteDate;
```

### Evaluate Automated Deletion Date
This script column is used to determine if Automated Delete Date is in the future. If in the future, then the result is true.


```
let status = true;

try
{
  let deleteDate = new Date(users['customSchemas_Tools4ever_DeleteDate']);
  let todayDate = new Date();

  if(todayDate > deleteDate)
  {
    status = false;
  }
  else
  {
  }

}
catch(e)
{
}


return status;
```


# NIM Docs
The official NIM documentation can be found at: https://docs.nimsuite.com
