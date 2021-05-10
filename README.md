### How to use [URL query params](https://docs.github.com/en/github/managing-your-work-on-github/about-automation-for-issues-and-pull-requests-with-query-parameters) + [a `config.yml` file](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository#configuring-the-template-chooser) to collect as much structured data as possible from the issue chooser

> <img src="https://user-images.githubusercontent.com/1469659/117646825-20431a00-b184-11eb-8601-2116e6a3a1e2.gif" width="650">

1. Create [a `config.yml` file](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository#configuring-the-template-chooser) on your repo
2. Populate the `contact_links` with URL query params. Here's an example:

```YAML
contact_links:
  - name: File an issue with structured data pre-filled
    url: https://github.com/lukehefson/all-the-structured-data/issues/new?assignees=lukehefson&labels=enhancement%2C+question&title=A+pre-filled+title&milestone=a+milestone&projects=lukehefson/all-the-structured-data/1
    about: Automate every bit of structured data possible upon issue submission
```

If you look at the above URL it breaks down like this:

| Part of the URL                                | What it does                                      |
|------------------------------------------------|---------------------------------------------------|
| github.com                                     | :octocat:                                         |
| /lukehefson                                    | User or Org name                                  |
| /all-the-structured-data                       | Repo name                                         |
| /issues/new?                                   | Create a new issue                                |
| assignees=lukehefson                           | Assign someone                                    |
| &labels=enhancement%2C+question                | (and) Add the `enhancement` and `question` labels |
| &title=A+pre-filled+title                      | (and) Pre-fill the title with some text           |
| &milestone=a+milestone                         | (and) Add it to a milestone                       |
| &projects=lukehefson/all-the-structured-data/1 | (and) Add it to a project board                   |
