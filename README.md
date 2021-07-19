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
 - A shared account will be managed by a grouper group - based on certrain group hierarchy. For example, gstlalcbc will be a nested group inside cbc group. And the CBC group managers (presumably the CBC group chairs) can then delegate the management of gstlalcbc to a particular user.
 - To do - do a tree diagram of this grouper group shared account structure. 
 - Should shared account have granularity cluster wise? For example, the lack granularity would mean a user satya having shared account access at CIT implying  also having shared account access at UWM and all other clusters. 
 - A sync script, like LGMM (cite here) will query the grouper stem for all the shared accounts, and associate the relevant shared account users with the correspnding  shared accounts, and write it periodically to the ldap. This script would use a delegated grouper web service call and bind to write at the master ldap.
 - The cluster admins can then obtain the shared account information from the ldap replica. 
 - Check how cluster admin currently provision the shared account (specially the SSH)
 - Should the cluster admin get a notification or the process should be fully automatic, as long as a grouper group manager assigns a user to a shared account group?
 - Check if there is a alredy usecase in the grouper community for using grouper for POSIX account management. 
