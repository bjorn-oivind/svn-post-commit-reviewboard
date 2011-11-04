# svn-post-commit-reviewboard

## Description

A quick hack to allow post commit review of commits which touches code in SVN. In the past I used a hacked up version of postreview.py, but that seems to have
broken after an upgrade to Review Board 1.6. It seemed like less work to do it from scratch in ruby instead, plus I get to sharpen my ruby "skills" some more :)

## Usage

Populate the variables at the top of the script with the correct values for your installation.

1.  @repo_url - should be the path of the repository as set in reviewboard.

3.  @reviewboard_url - should be the url to your reviewboard instance.

4.  @reviewboard_username - should be the username of a reviewboard user *with rights to submit as other users*.

5.  @reviewboard_password - should be the password for the given user.

Call the script either directly from SVN by installing it into the hooks-directory of your repository, or simply call
it from the existing post-commit script with the repository argument.
Install the necessary gems using bundle ("bundle install" or "bundle install --deployment")

## Written By

[Bjørn Øivind Bjørnsen](https://github.com/bjorn-oivind)
