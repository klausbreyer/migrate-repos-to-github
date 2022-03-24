# migrate repos to github
## Prerequisite

`brew install gh`

## Run
`(for d in */; do cd "${d%/}"; gh repo create "${d%/}" --private --source=. --remote=upstream && git branch -M main && git push -u upstream main; cd ..; done)` in directory with repositories you want to migrate to github.
