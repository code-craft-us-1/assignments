# Pass with Single Responsibility

Rapid cycles of test and development form the essence of TDD. Testing each functionality on its own makes it easy to add more functionality. This is one way of expressing Single Responsibility.

## The task

- Fix the bug and pass the tests, which are failing from the [previous assignment](fail.md).
- In your build-workflow (`.github/workflows/main-workflow.yml`), _remove_ `bash .github/workflows/expectfail.sh` in all places where it's present - otherwise passing tests will fail the Action.

## Observe

- Did the failing test describe the functionality you are fixing?
- Is every functionality getting tested? If some functionality is not reached by the test, you may be mixing responsibilites. Think Single Responsibility
- Does the workflow still fail after fixing the bug? Your test may be giving a false negative, or the workflow may have been failing for non-test reasons.
- Ensure that it's possible to call the production code without running the tests/asserts. You can do it by placing production code in a simple header file, or even move it into its own dll. 
