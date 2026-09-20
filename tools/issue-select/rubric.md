# Rubric: is this a good first issue?

<!--
THIS IS THE PART YOU WRITE. The skill in SKILL.md executes whatever checks
you define here. It ships empty on purpose: the judgment is your work.

A filled rubric must contain:

1. At least one row in the checks table. Each row needs all four columns:
   - Check: a short name (used in the output JSON).
   - Evidence: exactly what to look at, and where. Name the source
     (repo-facts block, issue body, comment thread, or the locations in
     references/evidence-guide.md). "The repo" is not a source; "the last
     5 default-branch commit dates" is.
   - Pass condition: a condition someone else could apply and get your
     answer. Prefer thresholds with numbers ("a maintainer commented
     within 30 days") over adjectives ("maintainer is responsive").
   - Weight: `required` (a fail here rejects the issue) or `preferred`
     (never changes the verdict; a nice-to-have that helps rank the
     issues you accept).

2. A verdict rule below the table: how the check grades combine into
   accept or reject, including how `unclear` is treated. The verdict
   space is binary. If you write no rule for `unclear`, the skill treats
   it as fail.

Cover what actually kills first contributions. The lecture named four
families: the maintainer is alive, the repo is in use, the scope fits a
newcomer, and nobody else is already on it. A rubric that ignores a family
will fail eval issues designed around that family.
-->

## Checks

| Check | Evidence | Pass condition | Weight |
|Maintainer activity|Recent default-branch commits, commit authors, and maintainer first-response sample from Repo facts.|Pass if there is evidence of human maintainer activity: at least one recent default-branch commit by a human OR at least one maintainer first response to an issue in the response sample. Fail if the repository shows no human maintainer activity in the available evidence.|required|
|Repository activity|Latest release, last push, archived status, and adoption signals in Repo facts.|Pass if the repository is not archived and there is evidence of recent activity, shown by a recent push or release. Fail if the repository is archived or there is no evidence of recent repository activity.|required|
|Bounded contribution scope|Issue body and comment thread. Look for umbrella/tracking issues, unresolved design debates, explicit references to major core-internal changes, and pure usage/support questions.|Pass if the issue describes a contribution that is one bounded piece of work and is not a pure usage question, umbrella/tracking issue, unresolved design decision, or explicitly stated core-internal redesign. Fail if any of those disqualifying conditions is present.|required|
|Existing work on the issue|Assignees, linked PRs, PRs mentioned in comments, and claim comments in the issue thread.|Pass if there is no active assignee, no open linked PR or other clearly active PR, and no clear evidence in the thread that someone is actively working on the issue. A closed/unmerged PR by itself does not fail this check if there is no current active work.|required|
|Contribution policy|CONTRIBUTING.md, .github/ contributor documentation, dedicated AI policy files, and issue/PR templates.|Pass if the repository has no stated restriction against AI-assisted contributions, or if its requirements can be followed. Fail if the repository explicitly prohibits AI-generated or AI-assisted contributions.|required|

## Verdict rule

<!-- State how the grades above combine into accept or reject, and how
unclear is treated. Example shape (write your own): "accept if every
required check passes; preferred checks never change the verdict, they
rank accepted issues; unclear counts as fail." -->

Accept the issue only if all required checks pass.

If any required check fails, the verdict is reject.

If a required check is unclear because the evidence needed by the check is genuinely absent, treat it as fail.
