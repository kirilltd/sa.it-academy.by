##14.Ansible.ws

```sh
PLAY [redmine] ******************************************************************************************************

TASK [Gathering Facts] **********************************************************************************************
Wednesday 07 April 2021  05:15:02 +0000 (0:00:00.102)       0:00:00.102 ******* 
ok: [redmine]

TASK [Redmine. Install packages] ************************************************************************************
Wednesday 07 April 2021  05:15:07 +0000 (0:00:05.169)       0:00:05.271 ******* 
ok: [redmine]

TASK [Redmine. Clone repository] ************************************************************************************
Wednesday 07 April 2021  05:15:13 +0000 (0:00:06.546)       0:00:11.818 ******* 
ok: [redmine]

TASK [Redmine. Change permissions] **********************************************************************************
Wednesday 07 April 2021  05:15:16 +0000 (0:00:02.169)       0:00:13.987 ******* 
ok: [redmine]

TASK [Redmine. Change permissions] **********************************************************************************
Wednesday 07 April 2021  05:15:18 +0000 (0:00:02.145)       0:00:16.133 ******* 
changed: [redmine]

TASK [db : MySQL. Install and setup] ********************************************************************************
Wednesday 07 April 2021  05:15:20 +0000 (0:00:01.932)       0:00:18.066 ******* 
changed: [redmine]

RUNNING HANDLER [db : mysql restart] ********************************************************************************
Wednesday 07 April 2021  05:15:24 +0000 (0:00:04.500)       0:00:22.566 ******* 
ok: [redmine]

TASK [db : Configuring encoding DB] *********************************************************************************
Wednesday 07 April 2021  05:15:27 +0000 (0:00:02.382)       0:00:24.948 ******* 
ok: [redmine]

TASK [db : Configuring user priviliges] *****************************************************************************
Wednesday 07 April 2021  05:15:29 +0000 (0:00:01.994)       0:00:26.943 ******* 
[WARNING]: Module did not set no_log for update_password
changed: [redmine]

TASK [db : Config database] *****************************************************************************************
Wednesday 07 April 2021  05:15:31 +0000 (0:00:02.033)       0:00:28.976 ******* 
changed: [redmine]

TASK [redmine : Redmine. Setup 01] **********************************************************************************
Wednesday 07 April 2021  05:15:35 +0000 (0:00:03.984)       0:00:32.961 ******* 
ok: [redmine]

TASK [redmine : Session store secret generation] ********************************************************************
Wednesday 07 April 2021  05:15:48 +0000 (0:00:13.012)       0:00:45.973 ******* 
ok: [redmine]

TASK [redmine : Redmine. Setup 02] **********************************************************************************
Wednesday 07 April 2021  05:15:50 +0000 (0:00:01.937)       0:00:47.911 ******* 
ok: [redmine]

TASK [redmine : Configuration files for virtualhost] ****************************************************************
Wednesday 07 April 2021  05:16:00 +0000 (0:00:10.893)       0:00:58.804 ******* 
changed: [redmine]

TASK [Add redmine-2.sa to host file] ********************************************************************************
Wednesday 07 April 2021  05:16:05 +0000 (0:00:04.073)       0:01:02.878 ******* 
ok: [redmine]

TASK [redmine : Check content] **************************************************************************************
Wednesday 07 April 2021  05:16:06 +0000 (0:00:01.775)       0:01:04.653 ******* 
ok: [redmine]

TASK [redmine : Replace host settings] ******************************************************************************
Wednesday 07 April 2021  05:16:13 +0000 (0:00:07.027)       0:01:11.680 ******* 
changed: [redmine]

RUNNING HANDLER [redmine : apache restart] **************************************************************************
Wednesday 07 April 2021  05:16:15 +0000 (0:00:02.155)       0:01:13.836 ******* 
changed: [redmine]

PLAY RECAP **********************************************************************************************************
redmine                    : ok=18   changed=7    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   

Wednesday 07 April 2021  05:16:20 +0000 (0:00:04.361)       0:01:18.197 ******* 
=============================================================================== 
redmine : Redmine. Setup 01 --------------------------------------------------------------------------------- 13.01s
redmine : Redmine. Setup 02 --------------------------------------------------------------------------------- 10.89s
redmine : Check content -------------------------------------------------------------------------------------- 7.03s
Redmine. Install packages ------------------------------------------------------------------------------------ 6.55s
Gathering Facts ---------------------------------------------------------------------------------------------- 5.17s
db : MySQL. Install and setup -------------------------------------------------------------------------------- 4.50s
redmine : apache restart ------------------------------------------------------------------------------------- 4.36s
redmine : Configuration files for virtualhost ---------------------------------------------------------------- 4.07s
db : Config database ----------------------------------------------------------------------------------------- 3.98s
db : mysql restart ------------------------------------------------------------------------------------------- 2.38s
Redmine. Clone repository ------------------------------------------------------------------------------------ 2.17s
redmine : Replace host settings ------------------------------------------------------------------------------ 2.16s
Redmine. Change permissions ---------------------------------------------------------------------------------- 2.15s
db : Configuring user priviliges ----------------------------------------------------------------------------- 2.03s
db : Configuring encoding DB --------------------------------------------------------------------------------- 1.99s
redmine : Session store secret generation -------------------------------------------------------------------- 1.94s
Redmine. Change permissions ---------------------------------------------------------------------------------- 1.93s
Add redmine-2.sa to host file -------------------------------------------------------------------------------- 1.78s
```