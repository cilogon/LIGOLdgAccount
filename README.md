#Assumes CO=IGWN

# IGWN cluster Account COmanage Registry Plugin
This plugin does the following things. 
 - Applying for a cluster account and provisoning to ldap
 - AUP signing record.
 - Authenticator management SSH, Certificate management, (SciTOKEN ?) at an UI and provisoning to ldap
 - Admin interface to manage shared account and provisoning to ldap


## 1. Applying for a cluster account 
 - Anyone with an active account CO:members:active could resuqest a cluster account. No approval needed. 
 - When CO:members:active is not then CO:COU:LDG Grid Account Holders:members:active becomes CO:COU:LDG Grid Account Holders:members:inactive
 - No Approval needed for cluster account creation
 - After accounts get created isMemberOf groups get updated - COMANAGE groups 
 
## 2. AUP signing is record is maitained at COMANAGE registry 
 - Currently only any older version of AUP agreed. Under current design  no new vewsion cannot be reagreed upon.
 
## 3. Authenticator management SSH, Certificate management at the UI and provisoning to ldap
  - Note - check the test COMANAGE to see if the SSH form could be adopted for certificate.
  - Authneticated certificate DN addtion to user's own record?
  - 
## 4. Admin interface to manage shared account and provisoning to ldap
 - Legacy non-standard cluster names?
