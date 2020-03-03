# Code Quality

## (CQ-100) High Maintainability

Requirements:

- All repositories *must* maintain their `master` branch at a Code Climate maintainability
  score of B or above.
- This score *must* be updated immediately after code is merged into the `master`
  branch.
- The maintainability score must be displayed near the top of the README at the
  root of the repository.

Rationale:

- Code Climate provides a robust and industry standard measure for the
  maintainability of a code base. While this is only one of many possible
  measures, Code Climate provides a solid baseline for measuring code quality.

Exceptions:

- The following types of repositories are excluded from this standard:
    - Data science repos containing only Jupyter Notebooks
    - Static websites not containing any code
    - Repos containing only programming languages not supported by Code Climate
- The following types of code can be excluded from your maintainability score:
    - Test code
    - Data migration code

---

## (CQ-110) Robust Test Coverage

Requirements:

- All repositories are required to maintain a code coverage level of 40%
  or higher for their `master` branch.
- Code coverage percentage *must* be published whenever code is pushed
  into the `master` branch.
- The code coverage percentage must be displayed near the top of the README at the
  root of the repository.
- All application code *must* be included in the coverage percentage, even if tests
  have yet to be written for the code.

Rationale:

- Code coverage is an indicator of how well test cases cover the codebase. While
  not a singular indicator of test quality, it is an important factor in ensuring
  that test cases cover a wide area of the codebase.

Exceptions:

- The following types of repositories are excluded from this standard:
    - Data science repos containing only Jupyter Notebooks
    - Static websites not containing any code
- The following code can be excluded from your test coverage percentage:
    - Test code
    - Data migration code

---

## (CQ-120) Code Cleanliness

When code is no longer wanted, delete it. Never commit commented out code.

Pull requests should not be approved until these comments have been removed.

Rationale:

- Standard git usage already tracks removed code so that it's not lost.
- Leaving commented code leave the code base `littered` with distractions to
  the actual code flow.

Exceptions:

- None
