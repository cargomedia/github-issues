# github-issues
`gi`is a command line tool to CRUD github issues. It maps every issue to a branch `issue-<issue-number>`.

The tool helps you to create these branches, work on them, and create pull-requests.


## Installation
### With [homebrew](http://mxcl.github.com/homebrew/)
```
brew tap cargomedia/cargomedia
brew install github-issues
```

### Manually
Download current version https://github.com/cargomedia/github-issues/tags and unpack.

Dependencies:
* ghi - https://github.com/stephencelis/ghi
* hub - https://github.com/defunkt/hub
* moreutils - http://joeyh.name/code/moreutils/
* coreutils (OSX only) - http://www.gnu.org/software/coreutils/

## Usage
```
usage: gi <command>

Commands:
  list [my]                 Lists repo's issues
  open [<message>]          Open a new issue
  checkout <issue-number>   Check out branch for specified issue, create it if needed
  details                   Show current branch-issue's details
  browse                    Open current branch-issue in web browser
  comment [<message>]       Add comment to current branch-issue
  push                      Push current branch-issue to origin
  pull-request [<target>]   Create a pull-request with the current branch-issue
```


## Workflow
Create a new issue:
```
gi open
```

Or start working on an existing issue:
```
gi checkout <issue-number>
```

..do some work, commit changes as usual (`git commit`)..

When your work is ready, push it to your origin and create a pull request:
```
gi push
gi pull-request
```

Before the pull request has been merged, you can push additional commits:
```
gi push
```
