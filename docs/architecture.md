# Application Architecture

## Overview

The application is a Flutter mobile app for Android and iOS.

The MVP uses local storage only and does not require a backend, user account,
or internet connection for its core functionality.

## Technology Stack

### Application Framework

- Flutter
- Dart

### Local Persistence

A local persistence solution will be selected before implementing permanent
product storage.

Possible options include:

- Isar
- Drift with SQLite
- Hive CE

The final decision must consider:

- package maintenance,
- Flutter compatibility,
- migration support,
- testability,
- support for structured product data,
- handling of local receipt file paths.

The chosen database package must be documented before implementation.

### Receipt Images

Receipt images will be captured or selected using maintained Flutter packages.

Images will be stored in the application's local file storage.

The database should store the local file reference rather than embedding large
image data directly into the product record unless a documented technical
reason requires otherwise.

### Notifications

Local deadline notifications will be implemented using a maintained Flutter
package that supports Android and iOS.

Notifications must not require a remote server.

## Architectural Principles

- Offline-first
- Local-only storage for the MVP
- Privacy by design
- Feature-based project structure
- Separation of UI, domain logic, and data access
- Testable business logic
- Small and focused widgets
- No unnecessary abstraction
- No premature backend preparation
- No functionality outside the current user story

## Proposed Project Structure

```text
lib/
├── app/
│   ├── app.dart
│   ├── routes.dart
│   └── theme/
│       ├── app_colors.dart
│       ├── app_spacing.dart
│       ├── app_text_styles.dart
│       └── app_theme.dart
├── core/
│   ├── errors/
│   ├── extensions/
│   ├── utils/
│   └── widgets/
├── features/
│   ├── products/
│   │   ├── data/
│   │   │   ├── models/
│   │   │   ├── repositories/
│   │   │   └── sources/
│   │   ├── domain/
│   │   │   ├── entities/
│   │   │   ├── repositories/
│   │   │   └── services/
│   │   └── presentation/
│   │       ├── screens/
│   │       ├── widgets/
│   │       └── controllers/
│   ├── receipts/
│   ├── deadlines/
│   ├── notifications/
│   └── consumer_information/
└── main.dart