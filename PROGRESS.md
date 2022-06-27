# Project Progress Tracker 

Here, I will log my weekly progress and learnings. This will be updated twice a week - on Monday and Thursday.  

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
- That would be a lot of files to test, so let's get this done.
- The focus would be on testing the behavious properly and not on the coverage as learnt earlier.
