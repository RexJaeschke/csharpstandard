## Understanding Branch draft-10-research

As of January 2024, TG2 is working on V8. In the background, Rex is working on fleshing out the MS proposals for Versions 9 and beyond, and creating lists of edits needed to add support for those features to the spec.

***The purpose of this branch is to store the work Rex has done for versions beyond V9, in a place accessible to TG2 officers, in the event that Rex is hit hard by a really big bus, or is otherwise unavailable to the committee.***

For V8, Rex's work has resulted in a set of (Draft) PRs in branch draft-v8. (Much of this work was done using various pre-V8 drafts.)

For V9, Rex's work has resulted in a set of (Draft) PRs in branch draft-v9 (which was derived from draft-v8 *just after it was created*, and before TG2 started work on V8).

Rex's work on V8 and V9 features may need tweaking (in small or large ways) if TG2 changes in substantive ways text in the spec upon which Rex's work was derived. For example, TG2 might add/remove/rearrange chapters, sections, and text within a section. While there is some risk in Rex's having used that approach, there will be more risk in trying to pin down *exactly* the edits needed for V10 and beyond. As such, Rex's V10 (and beyond) work has *not* been added as (Draft) V10 PRs. Rather, he has been saving that work in a DropBox folder to which Bill, Mads, and Jon have access. However, after a discussion with Bill, on Rex's fork, https://github.com/RexJaeschke/csharpstandard, Rex has created branch draft-v10-research as a place to store V10 (and beyond) files, so they reside in his fork where they are available to anyone who has access to his fork (such as Bill).

Here's how Rex does his spec research on his own machine, outside of GitHub:

- For each new version, Rex creates a folder with that version's name.
- For each new feature in a version, Rex creates a folder with that feature's name.
- That feature folder contains all files relating to spec'ing that feature. Typcially, it has (at least) the following:
  - One or more folders each containing a Visual Studio project used to test various aspects of the feature.
  - A Word (docx) file containing all the edits, notes, and issues for that feature. (See details below.)
- Once the feature's spec is (almost totally) complete, Rex creates a Draft PR for it by applying all the edits in the Word document to the repo. If at that time, tools find any problems w.r.t md formatting, code compilation and execution, and such, Rex addresses those via further Commits to that PR.

**The spec text in the docx file is written using md syntax** using pseudo-tracked changes to indicate insertions and deletions. It also uses various Word capabilities, such as header styles and a Table of Contents, color, and comments, to help the reader navigate the document, and in one place to be able to see all the changes to all the chapters. There may also be notes indicating issues to be created in GitHub or identified in the Draft PR cover. Chapters and sections that need work have their headings marked yellow. As each section's edits in a docx file have been applied to a Commit, their headings are marked green, which allows a Draft PR to be created over multiple Draft PR editing sessions.

At any time during the creaton of a feature's docx file, Rex can drop some/all of its contents into an md previewer to make sure the formatting is as intended. He can also extract any new/changed examples, and run them through the ExampleExtrator and ExampleTester tools, on his own machine.

At the folder top level, there is a feature-status file named "v*X*-feature-tracker.md". It tracks the status of Rex's research (and TG2's subseqeunt processing) on each feature. When the version research files are converted to a set of Draft PRs, this file should be added to the repo's main admin folder. (For example, when V8 is shipped, branch-v10 can be created, the Draft PRs for V10 can be created, and the feature-status copied to admin.)


