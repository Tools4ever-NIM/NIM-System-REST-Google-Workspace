# NIM-Conn-System-REST-Google-Workspace


This is a native rest connector. This repo is for additional tools specific to Google Workspace

## Table of Contents
* [Getting Started](#getting-started)
* [Automated Deletion](#automated-deletion)  

## Getting Started
* Create user account 
* Enable user account
* Disable user account
* Delete user account
* Group Membership (Add / Remove)

## Custom Schemas
If you need to import custom schema data into NIM you can extend the table schemas by adding a custom json file. 

C:\Program Files\Tools4ever\NIM\sysconfig\rest\systems\<SystemName>.json

<SystemName> = The name of the system in NIM.

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
