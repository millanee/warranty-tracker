# MVP Scope

## MVP Objective

The MVP should test whether consumers are willing to register purchases and
store receipts in an app in order to manage warranty and statutory rights
information.

The first version must remain small, offline-capable, and technically manageable
for a solo developer.

## Target Market

The MVP targets consumers in Germany.

## Supported Platforms

- Android
- iOS

The application will be developed using Flutter and Dart with one shared
codebase.

## Required MVP Features

### 1. Manual Product Registration

The user can manually enter:

- product name,
- category,
- purchase date,
- purchase price,
- retailer,
- manufacturer warranty duration.

All labels, validation messages, and buttons shown in the UI must be written
in German.

### 2. Receipt Capture

The user can:

- take a receipt photo using the device camera, or
- select an existing image from the device.

The receipt image is stored locally and linked to the corresponding product.

### 3. Local Product Storage

Product information and receipt references are stored locally on the device.

Stored products must remain available after the application is closed and
reopened.

### 4. Product Overview

The user can view a list of stored products.

Products may be grouped or visually categorized by status:

- expiring soon,
- active,
- expired.

The corresponding UI labels must be displayed in German.

### 5. Product Details

The user can open a stored product and view:

- product information,
- purchase information,
- receipt image,
- manufacturer warranty end date,
- statutory rights end date,
- current deadline status.

### 6. Deadline Calculation

The application calculates:

- the end date of the manufacturer warranty,
- the end date of the relevant statutory rights period.

The manufacturer warranty duration can be configured by the user.

The initial statutory rights logic is designed for the German market.

Legal assumptions must be documented and must not be silently hard-coded
without explanation.

### 7. Local Notifications

The application can schedule local notifications before a relevant deadline.

Initial reminder intervals:

- 90 days before,
- 30 days before,
- 7 days before.

Notifications must work without a backend.

### 8. Consumer Information Module

The application contains general information explaining:

- manufacturer warranties,
- statutory consumer rights,
- the difference between the two concepts.

The content must be written in clear German.

The application must explicitly state that the information is general consumer
information and not legal advice.

### 9. Complaint Checklist

The application provides a simple checklist for defective products.

Possible checklist items include:

- open the stored receipt,
- verify the purchase date,
- check the displayed deadlines,
- document the defect,
- contact the retailer or manufacturer,
- determine whether the case concerns a warranty or statutory rights.

The checklist shown to users must be written in German.

## Explicitly Excluded from the MVP

- No backend
- No user accounts
- No login
- No cloud synchronization
- No synchronization between devices
- No OCR receipt recognition
- No automatic email import
- No family sharing
- No automatic retailer contact
- No automatic complaint submission
- No binding legal assessment
- No individualized legal advice
- No support for countries outside Germany
- No web application
- No desktop application
- No subscription model
- No advertising during the initial development sprints

## Language Requirements

### Development Language

English must be used for:

- source code,
- file names,
- classes,
- functions,
- variables,
- code comments,
- technical documentation,
- GitHub issues,
- user stories,
- acceptance criteria,
- test names,
- commit messages,
- pull request descriptions,
- Cursor configuration,
- AI prompts.

### Application Language

German must be used for all user-facing content, including:

- screen titles,
- navigation labels,
- buttons,
- form labels,
- validation messages,
- empty states,
- error messages,
- notification content,
- information texts,
- complaint guidance.

## Scope Control

A feature outside this document must not be implemented unless it has first
been:

1. added to the Product Backlog,
2. described as a user story or technical task,
3. prioritized,
4. assigned to a sprint.

AI coding tools must not introduce features outside the active user story.