# Windows Shared Folder and User Access Administration

## Project Overview

This document describes my practical experience managing Windows shared folders, user access and file permissions in business environments.

The objective was to provide authorized users with reliable access to shared business files while preventing unauthorized access and maintaining continuity during system changes.

All company names, usernames, server names and production details are generalized for confidentiality.

## Business Requirement

Business users required centralized access to shared files for daily operations.

The environment needed to support:

- Shared access for approved users
- Separate access permissions for different teams
- Reliable network-drive connectivity
- Protection of confidential information
- Troubleshooting of unavailable folders
- Continuity during storage or computer changes

## Technologies Used

- Windows Server
- Active Directory
- Windows file sharing
- NTFS permissions
- Share permissions
- Security groups
- Windows client computers
- File servers
- Mapped network drives

## Tasks Performed

- Created and maintained shared folders
- Configured folder-sharing settings
- Applied NTFS permissions
- Assigned access to approved users and groups
- Removed unnecessary access
- Mapped shared folders on client computers
- Troubleshot unavailable network shares
- Checked network connectivity to the file server
- Verified user-account and group membership
- Maintained shared-folder availability during storage changes
- Tested user access after configuration changes
- Documented permissions and troubleshooting results

## Share and NTFS Permissions

Windows shared-folder access may be controlled through two permission layers:

| Permission Layer | Purpose |
|---|---|
| Share permissions | Control access when the folder is opened through the network |
| NTFS permissions | Control access to files and folders on the Windows file system |

The effective permission is determined by the combination of share and NTFS permissions.

## Example Sanitized Access Structure

```text
Shared Folder: Department-Documents

Administrators:
- Full Control

Department Managers:
- Modify
- Read and Execute
- List Folder Contents
- Read
- Write

Authorized Users:
- Read and Execute
- List Folder Contents
- Read

Unauthorized Users:
- No access
