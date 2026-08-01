# Definition of Done

A user story is considered Done only when all applicable conditions below are
satisfied.

## Functional Completion

- All acceptance criteria are satisfied.
- The implementation covers the complete intended user flow.
- No unrelated functionality was added.
- Error, empty, and validation states were considered where applicable.
- The implementation does not introduce known regressions.

## Design

- The implementation was compared with the linked Figma design.
- Layout, spacing, typography, and component structure reasonably match the
  approved design.
- User-facing text is written in German.
- Development identifiers remain in English.
- The UI works on relevant mobile screen sizes.
- Interactive elements have usable touch targets.
- Long or realistic German text does not break the layout.

## Code Quality

- Dart null safety is respected.
- Code follows the existing project structure.
- UI, business logic, and data access are separated where appropriate.
- No unnecessary package was added.
- No unrelated refactoring was performed.
- No dead code or temporary debugging output remains.
- Code is understandable and maintainable.
- English is used for code, comments, documentation, and identifiers.

## Verification

- `dart format .` has been executed.
- `flutter analyze` completes without errors.
- Relevant automated tests pass.
- New business logic has appropriate tests.
- Important UI behavior has appropriate widget tests.
- The feature was manually tested on an emulator or physical device.
- Every acceptance criterion was checked individually.

## Data and Privacy

- User data remains local unless the active story explicitly states otherwise.
- No backend or cloud functionality was introduced.
- No secrets, credentials, or private configuration files were committed.
- Sensitive receipt information is not written to application logs.
- Only necessary permissions are requested.

## Documentation

- Relevant documentation was updated.
- Important architectural decisions were documented.
- New package dependencies include a justification.
- Legal assumptions were not introduced without documentation.
- The GitHub issue contains enough information to understand the completed work.

## Version Control

- Changes are committed to the appropriate feature branch.
- Commit messages are written in English.
- The pull request references the relevant GitHub issue.
- The pull request describes the implementation and test results.
- The code diff was reviewed before merging.
- The completed work is available in the main repository branch.

## Completion Rule

A story must not be moved to Done when:

- tests are failing,
- Flutter analysis contains errors,
- acceptance criteria are only partially implemented,
- the implementation was not manually reviewed,
- unresolved defects prevent the intended user flow.

Incomplete work remains in progress or returns to the Product Backlog.