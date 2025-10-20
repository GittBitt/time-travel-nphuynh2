## Git Journal - 10/20/2025
I learned that a pull request needs commits; `gh pr create` fails if you only have uncommitted changes. I fixed this by running `git add .` to add current changed files, then
`git commit -m "commit message"`. 

One of my PRs was also meant to resolve an issue, but I didn't reference the issue in the body of the command. In order to merge a pull request
that actually resolves an issue, I first needed to know what number the issue was (like 1), then have a keyword like "fixes #1"
in the pr merge body, as shown here:`gh pr create --title "Title" --body "fixes #1" --base "main"`

Then, depending on the number of the PR (1 as an example), I can merge it with `gh pr merge 1`
