# How to use Github for "journal" reviews

Under the convention that authors known the names of their reviewers, then...

## Need some scripts to autogen some stuff

### PROBLEM 1: had navigation problems. 

_SOLUTION_

+ need to build links reviews <-> papers

### PROBLEM 2:  had personnel tracking problems. 

_ SOLUTION_

+ need to make the issues assigned to each reviewer seperate issues containing the review text
+ create milestones for for 1jan16, 1feb16, 1mar16, etc
+ assign due dates to those milestones (which can be reviewed first of each month

### Scripts

when "accepting" a paper, version N, for review, auto-create

- a directory for the corresponding author's last name
- a file in that directory called thatPaperTitleVN.md (camel case, no blanks)
    - labelled "1.new"
- an issue report called lastname/thatPaperTitleVN/reviews
    - with h1 title
    - with h2 url 
        - with URL to lastname/thatPaperTitleVN
    - with h2 entries for the review template
    - that ends with a list of 
        - "must do" (if not done, cannot accept), 
        - "should do" (arguably, improve the paper), 
        - "might do" (optinal suggestions)
        - editorial changes (typos)
- a file in that directory called thatPaperTileHistory.md
    - with h1 title
    - with h2 history
        - with a list whose top item is a pointer to the issue lastname/thatPaperTitleVN/reviews
        - with a list whose next item is a pointer to the file lastname/thatPaperTitleVN.md

then tell authors to write their paper into thatPaperTitleVN.md and relabelled in "2.submitted"

for all "submitted" papers, we must create

- one issue for each reviewer
    - assigned to the milestone with its due date.
    - assigned to that reviewer
    - with a pointer to the vN file and the vN review issues
    - NOTE: the actual reviewes are NOT written into this issue but into lastname/thatPaperTitleVN/reviews
- and the paper is labelled '3.underReview'

