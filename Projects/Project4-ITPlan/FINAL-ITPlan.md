### Creating OUs
```
![](![Screenshot 2024-04-17 191627](https://github.com/Fischbach23/CEG2410/assets/89490140/8347d510-12ac-4a2f-a485-c5ff199bbacd)

```


### Joining users
```
![](image.png)
```

### Joining Computers
```
![](image.png)
```

### Creating Groups
```
project_repos_RW - Security groups
finance_RW - Security groups
onboarding_R - Security groups
server_access - Servers
dev_eng_admins - Developers
hr_finance_admins - HR
remote_workstation - Workstation
```

## OUs & GPOs
```

Lock out Workstations after 15 minutes of inactivity. - Configure the "Interactive logon: Machine inactivity limit" policy setting under Computer Configuration > Policies > Administrative Templates > Control Panel > Personalization. (Link the GPO to the OU containing your workstation computers.)
Prevent execution of programs on computers in Secure OU - Configure the "Software Restriction Policies" under Computer Configuration > Policies > Windows Settings > Security Settings. (Link the GPO to the "Secure OU" containing your computers.)
Disable Guest account login to computers in Secure OU - Configure the "Accounts: Guest account status" policy setting under Computer Configuration > Policies > Windows Settings > Security Settings > Local Policies > Security Options. (Link the GPO to the "Secure OU" containing your computers.)
Allow server_access to sign on to Servers - onfigure the "Allow log on through Remote Desktop Services" policy setting under Computer Configuration > Policies > Windows Settings > Security Settings > Local Policies > User Rights Assignment. (Link the GPO to the OU containing your servers.)
Set Desktop background for Conference computers to company logo. - Configure the "Desktop Wallpaper" policy setting under User Configuration > Policies > Administrative Templates > Desktop > Desktop. (Link the GPO to the OU containing your conference computers.)
Allow users in remote_workstation group to RDP to Workstations - Configure the "Allow log on through Remote Desktop Services" policy setting under Computer Configuration > Policies > Windows Settings > Security Settings > Local Policies > User Rights Assignment. (Link the GPO to the OU containing your workstations.)
```

## Managing OUs

```
Right click on the OU, then click delegate control, then type in hr_finance_admins or end_dev_admins, then click add. then you get to choosewhich permissions they both have and I gave them both all permissions because they are overseeing the entire department they are a part of.



