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

Besides this, exists `development`, where functional code and merges are put, and `master` that contains a stable version.

## Releases versioning
![](https://img.icons8.com/dusk/100/000000/upgrade.png)
> The content of this section are extracted and adapted by [SemVer](https://semver.org/)  

Given a version number MAJOR.MINOR.PATCH, increment the:

- MAJOR version when you make incompatible API changes,  
- MINOR version when you add functionality in a backwards-compatible manner, and  
- PATCH version when you make backwards-compatible bug fixes.  

Additional labels for pre-release and build metadata are available as extensions to the MAJOR.MINOR.PATCH format.

## Keeping a good changelog
![](https://img.icons8.com/dusk/100/000000/overview-pages-4.png)
> The content of this section are extracted and adapted by [keep a changelog](https://keepachangelog.com/en/0.3.0/)

A good change log sticks to these principles:
- It’s made for humans, not machines, so legibility is crucial.
- Easy to link to any section (hence Markdown over plain text).
- One sub-section per version.
- List releases in reverse-chronological order (newest on top).
- Write all dates in YYYY-MM-DD format. (Example: 2012-06-02 for June 2nd, 2012.) It’s international, sensible, and language-independent.
- Explicitly mention whether the project follows [Semantic Versioning]().
- Each version should:  
  - List its release date in the above format.  
  - Group changes to describe their impact on the project, as follows:  
     `Added` for new features.  
      `Changed` for changes in existing functionality.  
      `Deprecated` for once-stable features removed in upcoming releases.  
      `Removed` for deprecated features removed in this release.  
      `Fixed` for any bug fixes.  
      `Security` to invite users to upgrade in case of vulnerabilities.
- in necessity case, it's possible add a metadada info, about recommendation or not of upgrade, like this:
```
1.0.2 2018-09-27 Update not required
Changed:
- gitignore updated with tmp directory

1.0.1 2018-09-27 Update recommended
Fixed:
- bug in parser
```
