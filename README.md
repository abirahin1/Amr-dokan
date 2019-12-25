name: Assign reviewers based on assignees
on:
  pull_request:
    types: [assigned, unassigned]

jobs:
  assignee_to_reviewer:
    runs-on: ubuntu-latest
    steps:
      - name: Assignee to Reviewer
        uses: pullreminders/assignee-to-reviewer-action@v1.0.4
        env:
          GITHUB_TOKEN: ${{ secrets.GI
