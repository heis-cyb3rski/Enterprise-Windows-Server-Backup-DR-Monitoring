# Enterprise Windows Server Backup, Disaster Recovery, and Monitoring Implementation

## Project Overview

This project demonstrates the implementation of a Windows Server backup, disaster recovery, and monitoring solution for a medium-sized organization with approximately 50 employees.

The objective was to establish a reliable backup strategy, automate backup operations, validate file recovery, verify available disaster recovery points, and monitor server performance and system events.

## Project Objectives

- Implement scheduled backups for business-critical data.
- Configure Windows Server System State backups.
- Automate backup operations using PowerShell.
- Test file recovery using Windows Server Backup.
- Verify available backup versions for disaster recovery.
- Monitor server performance and system events.

## Lab Environment

| Component | Configuration |
|---|---|
| Virtualization Platform | Microsoft Hyper-V |
| Operating System | Windows Server 2025 |
| Server Role | Active Directory Domain Controller |
| RAM | Hosted on a 16 GB RAM physical machine |
| Backup Destination | Dedicated virtual backup disk (E:) |
| Backup Tool | Windows Server Backup |
| Automation | PowerShell |
| Monitoring Tools | Performance Monitor and Event Viewer |

## Technologies Used

- Windows Server 2025
- Hyper-V
- Windows Server Backup
- PowerShell
- Task Scheduler
- Performance Monitor
- Event Viewer

## Implementation

### 1. Backup Storage Configuration

Prepared a dedicated backup storage volume labelled `SERVER_BACKUP` and assigned drive letter E:.

Installed and configured the Windows Server Backup feature.

### 2. Business Data Backup

Created sample business data representing different organizational departments:

- Human Resources
- Finance
- Operations
- Information Technology

Configured backups of the CompanyData directory.

### 3. System State Backup

Implemented a Windows Server System State backup to protect important server configuration information, including critical domain controller components.

Verified available backup versions using Windows Server Backup command-line tools.

### 4. PowerShell Backup Automation

Developed a PowerShell script to automate:

- Company data backups.
- System State backups.
- Backup logging.
- Basic execution error reporting.

Script location: `Scripts/AutomatedBackup.ps1`

### 5. Task Scheduler Configuration

Created a scheduled task named `Enterprise Automated Backup`.

Configured it to execute the PowerShell backup script automatically on a weekly schedule.

Verified the task configuration and initiated a test run.

### 6. File Recovery Testing

Used the Windows Server Backup Recovery Wizard to recover a sample business file.

The file was restored to an alternate location:

`C:\RecoveryTest`

Verified that the recovered file was available without overwriting the original.

### 7. Disaster Recovery Validation

Reviewed available backup versions and confirmed that recovery points were registered on the backup destination.

This provided evidence that previously completed backups were available for recovery.

### 8. Server Monitoring

Configured Performance Monitor to observe:

- Processor utilization.
- Available memory.
- Physical disk activity.

Used Event Viewer to review:

- System events.
- Application events.
- Errors and warnings.

## Project Validation

The following activities were completed:

| Test | Result |
|---|---|
| Business data backup | Completed |
| System State backup | Completed |
| Backup version verification | Completed |
| PowerShell script creation | Completed |
| Script syntax validation | Passed |
| Task Scheduler configuration | Completed |
| Scheduled task launch | Verified |
| File recovery to alternate location | Successful |
| Disaster recovery point verification | Completed |
| Performance monitoring configuration | Completed |
| Event Viewer review | Completed |

**Note:** The scheduled task was configured and its launch verified, but a complete successful scheduled execution was not independently confirmed. A full bare-metal server restoration was also outside the scope of this lab.

## Key Skills Demonstrated

- Windows Server Administration
- Backup and Recovery Management
- Active Directory Domain Controller Protection
- PowerShell Scripting
- Task Scheduler Configuration
- Disaster Recovery Planning
- File Recovery Testing
- Server Performance Monitoring
- Windows Event Log Analysis
- Technical Documentation

## Conclusion

This project demonstrates practical experience implementing backup and recovery processes, automating administrative tasks, validating file restoration, and monitoring Windows Server infrastructure.

It highlights the importance of protecting business-critical information, maintaining recoverable backup versions, and monitoring server health to support business continuity.

---

**Project:** Enterprise Windows Server Backup, Disaster Recovery, and Monitoring Implementation  
**Platform:** Windows Server 2025  
**Virtualization:** Hyper-V
