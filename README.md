# NIM-Conn-System-REST-Google-Workspace


This is a native rest connector. This repo is for additional tools specific to Google Workspace

## Table of Contents
* [Requirements](#requirements)
* [Authorization Scopes](#authorization-scopes)  
    * [Recommended Scope Sets](#recommended-scope-sets)  
* [Available Provisioning Actions](#available-provisioning-actions)
* [Custom Schemas](#custom-schemas)

# Requirements
* Google Account with Super Admin Role
* Service Account created via Cloud Console

## Authorization Scopes
|Table                                     |Scopes                                                          | Cloud Console                                             |
|------------------------------------------|----------------------------------------------------------------|------------------------------------------------------------------|
|chromeosdevices                           |https://www.googleapis.com/auth/admin.directory.device.chromeos |gcloud services enable admin.googleapis.com                       |
|classroom_courses                         |https://www.googleapis.com/auth/classroom.courses               |gcloud services enable classroom.googleapis.com                   |
|classroom_course_aliases                  |https://www.googleapis.com/auth/classroom.courses               |gcloud services enable classroom.googleapis.com                   |
|classroom_course_students                 |https://www.googleapis.com/auth/classroom.rosters               |gcloud services enable classroom.googleapis.com                   |
|classroom_course_teachers                 |https://www.googleapis.com/auth/classroom.rosters               |gcloud services enable classroom.googleapis.com                   |
|classroom_invitations                     |https://www.googleapis.com/auth/classroom.rosters               |gcloud services enable classroom.googleapis.com                   |
|classroom_userProfiles_guardianInvitations|https://www.googleapis.com/auth/classroom.guardianlinks.students|gcloud services enable classroom.googleapis.com                   |
|classroom_userProfiles_guardians          |https://www.googleapis.com/auth/classroom.guardianlinks.students|gcloud services enable classroom.googleapis.com                   |
|datatransfer_transfers                    |https://www.googleapis.com/auth/admin.datatransfer              |                                                                  |
|drive_drives                              |https://www.googleapis.com/auth/drive                           |gcloud services enable drive.googleapis.com                       |
|groups                                    |https://www.googleapis.com/auth/admin.directory.group           |gcloud services enable admin.googleapis.com                       |
|groups_aliases                            |https://www.googleapis.com/auth/admin.directory.group           |gcloud services enable admin.googleapis.com                       |
|groups_settings                           |https://www.googleapis.com/auth/apps.groups.settings            |gcloud services enable groupssettings.googleapis.com              |
|licenses                                  |                                                                |                                                                  |
|license_assignments                       |https://www.googleapis.com/auth/apps.licensing                  |gcloud services enable licensing.googleapis.com                   |
|members                                   |https://www.googleapis.com/auth/admin.directory.group           |gcloud services enable admin.googleapis.com                       |
|mobiledevices                             |https://www.googleapis.com/auth/admin.directory.device.mobile   |gcloud services enable admin.googleapis.com                       |
|orgunits                                  |https://www.googleapis.com/auth/admin.directory.orgunit         |gcloud services enable admin.googleapis.com                       |
|privileges                                |https://www.googleapis.com/auth/admin.directory.rolemanagement  |gcloud services enable admin.googleapis.com                       |
|roleAssignments                           |https://www.googleapis.com/auth/admin.directory.rolemanagement  |gcloud services enable admin.googleapis.com                       |
|roles                                     |https://www.googleapis.com/auth/admin.directory.rolemanagement  |gcloud services enable admin.googleapis.com                       |
|users                                     |https://www.googleapis.com/auth/admin.directory.user            |gcloud services enable admin.googleapis.com                       |
|users_aliases                             |https://www.googleapis.com/auth/admin.directory.user            |gcloud services enable admin.googleapis.com                       |
|users_asps                                |https://www.googleapis.com/auth/admin.directory.user.security   |gcloud services enable admin.googleapis.com                       |
|users_gmail_settings_autoforwarding       |https://www.googleapis.com/auth/gmail.settings.basic,https://www.googleapis.com/auth/gmail.settings.sharing             |gcloud services enable gmail.googleapis.com                       |
|users_gmail_settings_delegates            |https://www.googleapis.com/auth/gmail.settings.basic,https://www.googleapis.com/auth/gmail.settings.sharing             |gcloud services enable gmail.googleapis.com                       |
|users_gmail_settings_forwardingAddresses  |https://www.googleapis.com/auth/gmail.settings.basic,https://www.googleapis.com/auth/gmail.settings.sharing             |gcloud services enable gmail.googleapis.com                       |
|users_gmail_settings_imap                 |https://www.googleapis.com/auth/gmail.settings.basic            |gcloud services enable gmail.googleapis.com                       |
|users_gmail_settings_language             |https://www.googleapis.com/auth/gmail.settings.basic            |gcloud services enable gmail.googleapis.com                       |
|users_gmail_settings_pop                  |https://www.googleapis.com/auth/gmail.settings.basic            |gcloud services enable gmail.googleapis.com                       |
|users_gmail_settings_sendas               |https://www.googleapis.com/auth/gmail.settings.basic            |gcloud services enable gmail.googleapis.com                       |
|users_gmail_settings_vacation             |https://www.googleapis.com/auth/gmail.settings.basic            |gcloud services enable gmail.googleapis.com                       |
|users_tokens                              |https://www.googleapis.com/auth/admin.directory.user.security   |gcloud services enable admin.googleapis.com                       |
|users_verificationCodes                   |https://www.googleapis.com/auth/admin.directory.user.security   |gcloud services enable admin.googleapis.com                       |

### Recommended Scope Sets
* User Provisioning
    * ```https://www.googleapis.com/auth/admin.directory.user,https://www.googleapis.com/auth/admin.directory.group,https://www.googleapis.com/auth/admin.directory.orgunit```
    * Cloud Console Apps
        * ```gcloud services enable admin.googleapis.com```
* User Provisioning + Security 
    * ```https://www.googleapis.com/auth/admin.directory.user,https://www.googleapis.com/auth/admin.directory.group,https://www.googleapis.com/auth/admin.directory.orgunit,https://www.googleapis.com/auth/admin.directory.user.security```
    * Cloud Console Apps
        * ```gcloud services enable admin.googleapis.com```
* User Provisioning + Licensing
    * ```https://www.googleapis.com/auth/admin.directory.user,https://www.googleapis.com/auth/admin.directory.group,https://www.googleapis.com/auth/admin.directory.orgunit,https://www.googleapis.com/auth/apps.licensing```
    * Cloud Console Apps
        * ```gcloud services enable admin.googleapis.com```
        * ```gcloud services enable licensing.googleapis.com```
* User Provisioning + Licensing + Security
    *  ```https://www.googleapis.com/auth/admin.directory.user,https://www.googleapis.com/auth/admin.directory.group,https://www.googleapis.com/auth/admin.directory.orgunit,https://www.googleapis.com/auth/apps.licensing,https://www.googleapis.com/auth/admin.directory.user.security```
    * Cloud Console Apps
        * ```gcloud services enable admin.googleapis.com```
        * ```gcloud services enable licensing.googleapis.com```
* Classroom
    * ```https://www.googleapis.com/auth/classroom.courses,https://www.googleapis.com/auth/classroom.rosters,https://www.googleapis.com/auth/classroom.guardianlinks.students```
    * Cloud Console Apps
        * ```gcloud services enable classroom.googleapis.com```
    

## Available Provisioning Actions
* Chrome Devices
    * Update Chrome Device
* Classroom
    * Courses
        * Create/Update/Delete
    * Course Aliases
        * Create/Delete
    * Course Students
        * Add/Remove
    * Course Teachers
        * Add/Remove
    * Course Invitations
        * Create/Delete
    * Guardian Invitations
        * Create/Delete
    * Guardians
        * Delete
* Drive
    * Drive
        * Create/Delete
* Groups
    * Group
        * Create/Delete
    * Group Alias
        * Create/Delete
    * Group Settings
        * Update
    * Group Member
        * Add/Remove
* License Assignments
    * Add/Remove
* Mobile Devices
    * Delete
* Org Units
    * Create/Update/Delete
* Role Assignments
    * Add/Remove
* Users
    * User
        * Create/Update/Delete/Undelete
        * Sign out
        * Turn Off 2FA
        * Delete Tokens
    * Alias
        * Add/Remove
    * Application Specific Passwords
        * Delete
    * Vertification Codes
        * Create/Delete
* Gmail
    * Auto Forwarding
        * Update
    * Delegates
        * Create/Delete
    * Forwarding Address
        * Create/Delete
    * IMAP
        * Update
    * POP
        * Update
    * Send As
        * Update
    * Vacation
        * Update


## Custom Schemas
If you need to import custom schema data into NIM you can extend the table schemas by adding a custom json file. 

C:\ProgramData\Tools4ever\NIM\config\rest\systems\SYSTEMNAME.json

SYSTEMNAME = The name of the system in NIM.

```
{
	"schema": {
		"crud_objects": {
			"users": {
				"resources": {
					"customSchemas": {
						"Tools4ever": {
							"ID":"_:string*",
							"Type":"_:string*",
							"DeleteDate":"_:string*"
						}
					}
				}
			}
		}
	}
}
```


# NIM Docs
The official NIM documentation can be found at: https://docs.nimsuite.com
