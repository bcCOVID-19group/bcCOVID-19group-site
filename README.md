[![Netlify Status](https://api.netlify.com/api/v1/badges/b746df38-2c47-409c-9ade-e35d442e20dd/deploy-status)](https://app.netlify.com/sites/silly-brahmagupta-1f7d22/deploys)

The bccovid-19group.ca site is running a version of the Academic Hugo Theme/system. This post provides an overview on how to contribute to the site and how the site can be used to support the research organization. (This content also appears in the README.md file.)

## How to contribute to website development?

### Clone repo and submodules

```bash
git clone https://github.com/bcCOVID-19group/bcCOVID-19group-site.git
git submodule update --init --recursive
```

> The submodule command should only need to be run once after cloning.

### Use git

+ Make changes in a branch. Push to GitHub. Pull request.
+ Deployments are handled by Netlify.
+ Branches are available for preview before merging pull requests. 

![screencap](https://wwejubwfy.s3.amazonaws.com/update_users_create_templates_by_colliand__Pull_Request_3__bcCOVID-19groupbcCOVID-19group-site_2020-04-07_18-02-56.png)

## How does the research organization work?

This site is designed to support a team of people (called `authors`) to collaborate on `projects` while producing outputs (`posts`, `publications`) that can be shared on the web. The content is developed in Markdown (and potentially R Markdown) files with YAML top matter.

### Team

The `authors` (subdirectory of `content`) has a tree structure that looks like this:

```
authors
├── admin
│   ├── _index.md
│   ├── avatar.png
│   └── old_avatar.jpg
├── carolinecolijn
│   ├── _index.md
│   └── avatar.jpg
├── colliand
│   ├── _index.md
│   └── avatar.jpg
├── dancoombs
│   ├── _index.md
│   └── avatar.jpg
└── ianabc
    ├── _index.md
    └── avatar.jpg

5 directories, 11 files
```

The file `_index.md` inside `_carolinecolijn` controls the content that appears on this person's page. (Author pages for other members of the Group need to be created.)

The people in the site can belong to groups (`Researchers`, `Support`) and are sorted accordingly on the `Team` page. 

### Projects

The files in the `project` directory describe a project for the Group. While carrying out work on a project, collaborators will generate outputs (`posts`, `publications`).



### Outputs

+ Posts
+ Publications

(We could also add `Talks`)
