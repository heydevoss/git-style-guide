# git-style-guide
Git styleguide followed by us here at panelinha-de-es

## Naming github branches
![](https://img.icons8.com/dusk/100/000000/code-fork.png)

Create a branch name, with the type of implementation, ID number of the GitHub issue, and a small description(separated by dash) about the issue, in the following style:  
`type/issue_id-small-description`  

```
# good
$ git checkout -b feature/12-implement-user-chart

# good: using identifiers
$ git checkout -b fix/27-apollo-server-invalid-query

# bad: too vague
$ git checkout -b login_fix
# bad: no use of dashes
$ git checkout -b feature/add_webhook
```

The possible types of branches are:
- *feat*: A new feature
- *fix*: A bug fix
- *docs*: Documentation only changes
- *style*: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
- *refactor*: A code change that neither fixes a bug nor adds a feature
- *test*: Adding missing or correcting existing tests

