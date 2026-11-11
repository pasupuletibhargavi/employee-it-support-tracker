# Employee IT Support Tracker

A scoped ServiceNow application for managing employee IT
support requests, automating assignment, enforcing
record-level access, and monitoring operational performance.

## Features
- Custom Employee IT Support Request table and form
- Automatic assignment of Software requests to the Software group
- 48-hour automated closure of requests that remain Resolved
- Role-based access controls with ownership-aware record editing
- Reports showing requests by status and priority
- Operations dashboard for support request monitoring

## Technologies
ServiceNow Studio, ITSM concepts, Flow Designer,
Business Rules, GlideRecord, ACLs, Platform Analytics, GitHub.

## Automation
1. A before-insert Business Rule assigns qualifying Software
   requests to the Software group when Assignment Group is empty.
2. An active Flow waits 48 hours after a request is resolved,
   rechecks its status, and closes it only if it remains resolved.

## Security
ACLs restrict record operations by application role and record
ownership. Testing confirmed that Joe Employee could edit an
owned request but could not edit it after the Employee field
was changed to another user.

## Validation
- Successfully tested automatic request closure
- Verified ownership-based editing restrictions
- Confirmed dashboard charts for status and priority

## Deployment
Developed in a ServiceNow Personal Developer Instance.
Application configuration is captured in an update set
for versioning and transport.

## Project Status
Core application features implemented and tested.
GitHub documentation and packaging are being finalized.
