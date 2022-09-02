Themes: [[Windows]], [[Networking]], 

# Workgroups
- Accounts required for each computer, no single computer has control
- All computers must be on the same local network
# Domains
- A structure containing computer and user accounts, all registered with a central database known as a domain controller

# Windows server administration tools
- Remote Server Administration Tools (RSAT)
- Allows you to manage a server remotely from a client - you should never manage a server from within the server

# Active Directory
- Directory services store, organise and provide access to information in a directory
- Active Directory allows you to organise network resources, including users, groups, printers, computers and other objects
- You can assign who can manage a group of objects

# User accounts
- Create a user group
- Assign permissions to the group
- Add and remove users from the group when needed
## Distribution groups
- Used to create email distribution lists, not for assigning permissions
## Group scope
- Determines how large a group (forest, tree) is

# Organisational Units (OUs)
- Containers which can be used to organise administration tasks in a domain
- Can store computers, users, groups etc
- Another grouping method to easily apply policies to multiple users/computers

# Kerberos Authentication
![[Pasted image 20220720101741.png]]
- Kerberos tickets can be stolen with Mimikatz

# File permissions
- By default, a child folder will inherit all permissions from its parent
