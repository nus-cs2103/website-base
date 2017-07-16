Note that project grading is ==not competitive (not bell curved)==. ==CS2103T projects will be assessed separately from CS2103 projects.== This is to account for the perceived difference in workload. Given below is the marking scheme.

**Total**: 50 marks (25 individual marks + 25 team marks)

1.  **Product features** [team][10 marks] - How good is your software as a product?

    Based on the features implemented, how well they fit together to make a good product, and how well they are demonstrated.

    ‘Half-baked’ (i.e. not production quality) or 'ill-fitting' (feature does not go well with the other features) features will not earn marks at all and could even be penalized. It may be better to remove such features before submission.

2.  **Design** [individual][5 marks] - How good is your internal design?

    Evaluated ==solely based on what we can learn from the developer guide.== Evaluated by lecturer. You will be graded individually on the design of your component and how well you have described it. Collective design decisions such as architecture will affect the grade of all team members.

    Criteria considered:
    *   Conformance with the multi-level top-down approach (i.e. design at high-level first, and do the lower-level design of each component later)
    *   Conformance with the OO paradigm
    *   Application of patterns and principles
    *   Quality of documentation e.g. using the right diagram at the right place.
3.  **Implementation** [individual][15 marks] - How good is your implementation? A measure of the ==quality and the quantity== of code you have written yourself. On average, a student is expected to write 0.5-1.5 KLoC. Evaluated based on an inspection of the collated code (submitted in your *.md files) by at least two tutors.  
    Criteria considered:
    *   Following SLAP (IMPORTANT).
    *   Following the coding standard given (IMPORTANT).
    *   Using at least some assertions.
    *   Using at least some logging.
    *   Using at least some unit tests.
    *   Commenting at the right level.
    *   Exception handling.
    *   Neatness and human readability.Expectations:
    *   Each person is expected to implement one or more features individually in addition to features implemented collectively. Each person is expected to write backend code, frontend code, test code, user documentation, and developer documentation.
4.  **QA** [team: 5 marks], [individual: 5 marks] - How good is your Quality Assurance? Evaluated based on our own testing. A well written user guide and a product that conforms to the user guide (i.e. no bugs) will give you a high mark.

    Things considered for team grade: Bugs including validation issues (i.e. not meeting project requirements)

    Things considered for individual grade: Quality and quantity of the test code in your collated code.

Expectations:

*   There is no requirement for a minimum coverage level. Note that in a production environment you are often required to have at least 90% of the code covered by tests. In this project, it can be less.
*   How much of each type of testing should you do? We expect you to decide. You learned different types of testing and what they try to achieve. Based on that, you should decide how much of each type is required. Similarly, you can decide to what extent you want to automate tests, depending on the benefits and the effort required.
*   Applying TDD is optional. If you plan to test something, it is better to apply TDD because TDD ensures that you write functional code in a testable way. If you do it the normal way, you often find that it is hard to test the functional code because the code has low testability.

7.  **Documentation** [team][5 marks] - How well does your user guide achieves its objectives? Evaluated by lecturer and TA.  
    Criteria considered:
    *   Explanation should be clear and written to match the audience.
    *   Good use of visuals to complement text.Note: Developer Guide is graded under the 'Design' component.
8.  **Project management** [team: 5 marks][individual: 5 marks] - How well you worked together as a team to follow a systematic process?  
    For the team component, we look for,
    *   Good version control, based on the repo.
    *   Good task definition, assignment and tracking, based on the issue tracker.
    *   Good use of buffers (opposite: everything at the last minute)
    *   Iterative (opposite: fake iterative, doing most of the work in one iteration).  
        Passed almost all checkpoints from V0.0 to V0.5The individual component is determined by peer evaluation from your project team members.

**Penalty for late submission:** ==-1 mark for each hour delayed.== Even a 1-second delay is penalized, irrespective of the reason. Based on the time shown by IVLE.