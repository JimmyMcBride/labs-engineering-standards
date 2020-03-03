# Node.js

## (NJ-100) Approved Package Managers

Only the following Node.js package managers are approved for projects in Labs:

- [NPM](https://docs.npmjs.com/)
    - Version > 6.0.0
- [Yarn](https://yarnpkg.com/)
    - Version > 2.0.0
    - *Preferred*

Rationale:

- Well executed package management is a crucial to the realization of a stable
  and consistent Node-based product. Only mature and stable package managers are
  permitted on Labs projects.

Alternatives:

- None

Exceptions:

- None

---

## (NJ-110) Approved Testing Frameworks

Only the following Node.js teting frameworks are approved for projects in Labs:

- [Jest](https://jestjs.io/)
    - Version > 25

Not permitted:

- Mocha, Jasmine

Rationale:

- While there are many valid ways to test a Node.js based application, we want
  limit the test frameworks in use so that we can maximize the opportunity for
  sharing of knowledge and tools.
- Jest provides a robust and well supported feature set that allows it to perform
  many different tasks without requiring many additional libraries.

Alternatives:

- None

Exceptions:

- None

Notes:

- This standard does _not_ exclude the use of various Jest plugins or compatible
  utility packages. For example, using SuperTest with Jest is perfectly acceptable
  as Jest is still the underlying test framework and SuperTest is simply an augmentation.
