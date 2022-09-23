# Work Summary

This includes the work that I did during **Google Summer of Code 2022** at project **Phoenix** under org **CERN-HSF**.

1. Writing unit tests for the [`phoenix-event-display`](https://www.npmjs.com/package/phoenix-event-display) library using Jest.
2. Migrating the unit tests for [`phoenix-app`](https://github.com/HSF/phoenix/tree/master/packages/phoenix-ng/projects/phoenix-app) (Phoenix application) and [`phoenix-ui-components`](https://github.com/HSF/phoenix/tree/master/packages/phoenix-ng/projects/phoenix-ui-components) (UI components used by the Phoenix application) to Jest from Jasmine and Karma. 
3. Writing end-to-end tests for Phoenix application using Cypress.

The Pull requests on which I worked and a brief summary of the work done (period-wise) -  

1. **Before the coding period**: *I read the documentation related to Phoenix (Phoenix Developer Guides) to get a knack of the things I will need to work upon throughout the project.*
   - https://github.com/HSF/phoenix/pull/409 [Remove and update Developer guides with the correct links]
   - https://github.com/HSF/phoenix/pull/410 [Add 'start' clipping angle as well as opening angle]
   - https://github.com/HSF/phoenix/pull/417 [Fix failing tests for ThreeManager and UIManager for stable CI job]

2. **During the community bonding period**: *During this period, I focussed on reading documentation related to the technologies that I would be using throughout the project and tried solving issues.*
   - https://github.com/HSF/phoenix/pull/436 [Update documentation for managers]
   - https://github.com/HSF/phoenix/pull/437 [Fix failing tests for ThreeManager]

3. **Coding Period - I**: *The major goal of this period was to complete writing new unit tests for `phoenix-event-display` and `phoenix-ng` and migrate existing ones inside `phoenix-ng`*.
   - https://github.com/HSF/phoenix/pull/462 [Add unit tests for lib and helpers inside `phoenix-event-display`]
   - https://github.com/HSF/phoenix/pull/473 [Add unit tests for loaders and managers inside `phoenix-event-display`]
   - https://github.com/HSF/phoenix/pull/491 [Use Jest for unit testing in `phoenix-ng` - I]

4. **Coding Period - II**: *With migration almost ready and the tests executing fine locally, some of the unit tests failed on the CI and hence, the issues on which I focussed in this period was to create a stable unit testing setup keeping in mind the CI environment - one using Jest and the other using Jasmine and Karma and then, we agreed mutually that the Jest setup would be better for the long run. End-to-end tests using Cypress for Phoenix application were also added.* 
   - https://github.com/HSF/phoenix/pull/492 [Use Jest for unit tests in Phoenix]
   - https://github.com/HSF/phoenix/pull/495 [Add e2e tests for Phoenix App]

5. **Future goals**: *Write documentation for the new testing infra for Phoenix. Add more unit tests for `phoenix-event-display/src/managers` as that needs completely mocking the WebGLRenderer.*  

Additional Links - 
- Project Roadmap: https://github.com/DamianArado/GSoC-2022-Phoenix/blob/main/ROADMAP.md
- Detailed Progress report and learnings: https://github.com/DamianArado/GSoC-2022-Phoenix/blob/main/PROGRESS.md
- Basic details about the project: https://github.com/DamianArado/GSoC-2022-Phoenix/blob/main/README.md

Thanks a lot for reading and I wish you a great year ahead! ^_^
