# Project Progress Tracker 

Here, I will log my weekly progress and learnings. This will be updated twice a week.

### Week 1 (May 30 - June 5, 2022)  

- Introductory video chat between the mentors and me in order to get to know each other and the work we do.
- Read about the testing framework which is better to use (faster execution, easy configuration, and maintenance) in order to refine the project plan.
- Divide the project deliverables into smaller parts.
- Finalize estimated deadlines and milestones.
- Try to figure out potential issues that may occur beforehand.
- Ask Ed & Fawad whether they agree to the milestones and if they have any doubts/questions for me (asking for feedback).
- Agree with Ed & Fawad on the way of communication throughout the project duration.

### Week 2 (June 6 - 12, 2022)  

- This week would be full of reading documentation and guides in order to make sure I don't lack the required theoretical knowledge for starting the project properly.
- Be in sync with the project regularly in order to avoid merge conflicts in future and my setup is ready on Windows 11 and I'll use VS Code. I don't have any problems reproducing the required development environment of Phoenix.
- Read about TypeScript and Angular - just a quick refresher.
- Read in-depth about the **general unit and integration testing conventions**.
- Read about Jasmine and Jest as from the next week, I would be rewriting the unit tests of *`phoenix-event-display`* that were written in Jasmine to use Jest. 
- Create issues that need to be solved as a part of the [first Coding period](https://github.com/DamianArado/GSoC-2022-Phoenix/blob/main/ROADMAP.md#coding-period---i).
- Ask for the target branches where I need to merge my changes done in *`phoenix-event-display`* and create source branches in my own fork.
- Try to test a few modules using Jest myself locally before introducing it in *`phoenix-event-display`*.

### Week 3 (June 13 - 19, 2022)  

- Remove Jasmine and Karma setup and add Jest-based setup.
- Start writing unit tests using Jest for *`phoenix-event-display`*.  
- Throughout the week, the plan is to complete writing tests for the module [`managers`](https://github.com/HSF/phoenix/tree/master/packages/phoenix-event-display/src/managers). 
- All the work is being done on the branch [**`jest-phoenix-event-display`**](https://github.com/DamianArado/phoenix/tree/jest-phoenix-event-display)  
- After some initial jitters and conflict between `@types/jasmine` and `@types/jest`, I have removed `@types/jasmine` for the time-being so that proper jest config has been setup, Continuing the work as planned above.  
- With the help of Fawad (a big thanks to him for helping me out with this), I was able to get rid of errors that made it difficult for the tests to run locally.  

### Week 4 (June 20 - 26, 2022)  

- Write tests for `helpers`, `lib` and `managers` (It was not as easy as I thought).
- The initial goal is to try and write unit tests for each file inside *`phoenix-event-display`*.  
- And after that, I will focus on increasing the code coverage.  
- Hence, initially the code coverage would be low.  
- I realized a very important thing as pointed out accurately by Fawad that I was focussing on the wrong thing – increasing code coverage of each of the modules but instead I should focus on testing the behavior of each unit (class, function, etc) properly and that will itself increase the overall code coverage.  
- Also, I got to know from Fawad, how to test static functions: instead of mocking them, we should treat them as standalone functions.
- Submitted PR for the week: https://github.com/HSF/phoenix/pull/462  

### Week 5 (June 27 - July 3, 2022)  

- Throughout this week, I plan to write unit tests for [`managers`](https://github.com/HSF/phoenix/tree/master/packages/phoenix-event-display/src/managers) and [`loaders`](https://github.com/HSF/phoenix/tree/master/packages/phoenix-event-display/src/loaders).  
- The focus would be *on testing the behavious properly and not on the coverage* as learnt earlier.
- I faced a big issue where tests that used `WebGLRenderer` as a dependency were not able to run at all as its not possible to create a `WebGLContext` in jest tests and after researching a bit alongwith Fawad, I got to know that I have to mock WebGLRenderer but that lead to objects of WebGLRenderer being `undefined`. As a workaround, I added a helper function `createRenderer` that makes it easy to use objects of WebGLRenderer in our tests.
- Wrote test cases for majority of the files in `managers`. Just facing difficulties in testing `ThreeManager` and `UIManager` classes as they use WebGLRenderer as a dependency. Need to find a way out.
- After writing unit tests for `loaders`, I plan to devote time to `ThreeManager` and `UIManager` specifically.
- And after that, the test suite for each eligible file inside `phoenix-event-display` would be ready and sent to be reviewed via a PR. 
- Submitted PR for the week: https://github.com/HSF/phoenix/pull/473

### Week 6 (July 4 - 10, 2022)

- Its the 4th week of the coding period and by that, I meant the first deliverable of my project, i.e., to write unit tests for *`phoenix-event-display`* would have to be completed. So, I'll be treating this week as a deadline for that.
- In the last PR, I did make a few mistakes of writing trivial test cases that used `spies` a lot but thanks Fawad for his proper review, I realised that I was actually not testing the methods and objects accurately.
- Hence, currently I'm working to update each and every test suite in the last PR.
- After this, I would be revisiting the remaining files again and would add/update/remove things accordingly.
- Still working on the last PR, should be ready by Friday. All thanks to Fawad, I could enhance the test suites due to his eye for details. His code review helps me a lot everytime.
- The last PR is still to be reviewed, so I started working on the next PR.

### Week 7 (July 11 - 17, 2022)

- With the next PR, I plan to add tests for some of the files which were left untested earlier in *`phoenix-event-display`*.
- Also, from this week, I'll be starting to work on the unit tests for *`phoenix-ui-components`* and *`phoenix-app`* which is the second milestone for the project.
- I will also analyze whether we can/we should convert all the unit tests here to use Jest or not.
- Thankfully, due to superb code reviews by Fawad, I'm able to finish writing unit tests in *`phoenix-event-display`*. Only a couple of them remains to be written - `three-manager/index.ts` and `ui-manager/index.ts` and they will involve heavy mocking due to the inability of creating `WebGLContext` in tests (as both `three-manager` & `ui-manager` have `WebGLRenderer` as a dependency). `JSDom` environment in Jest doesn't use a real DOM, it just emulates one, and it can be a potential issue in testing three.js with Jest. But apart from this, I had a good first experience with Jest here.
- By this week, I plan to update the setup of *`phoenix-ui-components`* and *`phoenix-app`* to use Jest for unit testing as well so that we have uniformity in the unit testing framework, that we use throughout Phoenix. But before that, I'll try setting up the configuration properly and see how it goes.

### Week 8 (July 18 - 24, 2022)

- The initial setup for the migration of unit tests inside *`phoenix-ui-components`* and *`phoenix-app`* is ready and is available at this  branch [**`jest-phoenix-app`**](https://github.com/DamianArado/phoenix/tree/jest-phoenix-app).
- This also involved changes in the module  structure inside *`phoenix-ng`*.
- All the old tests do run using Jest but they are throwing up errors as of now. Hopefully, that can be fixed. 
- Throughout this week, my focus would be to work on the unit-testing setup of *`phoenix-ng`*.
- I proposed that we should only use Jest for our unit tests and since, we will not use Protractor for our end-to-end tests, there is no requirement for Jasmine or Karma now. Let's wait for the feedback from Fawad and Ed as to whether this is good for Phoenix or not.

### Week 9 (July 25 - 31, 2022)

- We have `midterm evaluation` this week and as of now, I'm working on the migration of unit tests inside *`phoenix-ng`* to Jest. Hoping to finish this by the end of the week.
- This seemed quite trivial to me at the start but here, I was bewildered with lengths and breadths of errors that showed up throughout the setup of Jest configuration inside the Angular project. Main ones being the `three/examples/jsm` files (yet again!).
- Firstly, I tried having separate jest config for each of *`phoenix-ui-components`* and *`phoenix-app`* but then, I thought of merging both the config as a single one inside *`phoenix-ng`*. 
- Jest and Jasmine APIs are quite compatible so that is a relief for me and some of the tests do pass. But the major issue here is created by `tweenjs` which is imported inside `controls-manager`. A lot of the tests inside `phoenix-ng` fail due to this import. Tried adding dependencies and module declaration file but it didn't fix that. Hoping to find out a solution soon.
- Submitted PR for the week: https://github.com/HSF/phoenix/pull/491

### Week 10 (August 1 - 7, 2022)  

- Later last week, some significant changes were made that included a merger of branches `jest-phoenix-event-display` and `jest-phoenix-app` into the new branch `jest-ng`. This will help us to make sure that we don't encounter any conflict hell (yikes!) in future and we will keep it in sync with `master` branch.
- `jest-phoenix-app` has been renamed to `jest-ng` and then `jest-phoenix-event-display` has been merged into it.
- All thanks to fawad, the tweenjs error was gone after the aforementioned merging of branches and I was able to start the migration of the testing suites inside `phoenix-ng` from `Jasmine` to `Jest`.
- From now on, all the changes that are to be committed by me for the project will be done on [`jest-ng`](https://github.com/HSF/phoenix/tree/jest-ng).
- When I started the migration, most of tests failed as they called the "real" Angular services instead of the fake ones.
- After extensive mocking, I am successfully able to migrate `46 out of the 54 testing suites` inside `phoenix-app` and `phoenix-ui-components`. I also increased the overall coverage by adding more test cases.
- For now, I have `skipped those 8 test suites` and plan to fix them one-by-one as they are somewhat complex.

### Week 11 - 12 (August 8 - 21, 2022)

- Except the 2 test suites inside `phoenix-ng`, all the remaining ones have been successfully migrated to Jest from Jasmine.
- Right now, I'm just stuck with an issue that the Jest tests run fine locally but 3 of them in `phoenix-event-display` (`SelectionManager`, `EffectsManager` and `XrManager` won't run as they use `WebGLRenderer` (yeah, it's back to annoy me again!). 
- I'm trying to find a way to create the required environment (possibly a [`headless-gl`](https://github.com/descriptinc/headless-gl) based environment) for these tests to execute themselves successfully on the CI.
- The submitted PR that has been continuing since more than a week: https://github.com/HSF/phoenix/pull/492
- By this week, I plan to get this PR merged and send one more with e2e tests that I'm currently working on locally as well.
