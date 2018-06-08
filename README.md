# The IIM(I2M) website, made using Jekyll.

Before using Jekyll, Ruby(with DEVKIT) should be installed. 

This site is designed to make it easy to add small updates, like adding:
- new members
- old members
- news
- projects
- publications

It just involves updating the right yaml file, and putting images in the right directory.

If you want to make larger changes to the site, like adding a new type of page, it will require more work.

            
# Updating the site (using git)
To update the site, you will need some familiarity with git. If you don't, brush up first.

First, you need to clone it:

```
git clone https://github.com/vincent-qin/vincent-qin.github.io.git
```

If you have already cloned the repo, make sure your copy of the repo is up-to-date:

```
git pull origin master
```

Next make changes to the files. Once you are done: add, commit, and push the changes:

```
git add .
git commit -m 'Description.'
git push origin master
```

## Small updates

### Members
To add a new member, edit `./_data/members.yml`. Add a new entry at the end of the file in the form:

```
- name: Shiyu Chang
  image: shiyu.jpg
  text:
  social:
    - title: envelope #use for email address
      url: mailto:chang87@illinois.edu
    - title: link
      url: http://www.ifp.illinois.edu/~chang87/
```

Then move the picture into `./assets/img/members`.

When you are done, push the changes.

### Past Members
To add a past member, edit `./_data/past_members.yml`. Add a new entry at the end of the file in the form:

```
- name: Ashutosh Garg
  job: Bloomreach Inc.
  email: ashutosh@ifp.uiuc.edu
  url: http://www.ifp.illinois.edu/~ashutosh/
```

When you are done, push the changes.


### Projects
To add a new project, edit `./_data/projects.yml`. Add a new entry at the end of the file in the form:

```
- name: Project Name
  image: project-figure-name.png
  text: 'Description.'
```

Then move the picture into `./assets/img/projects`.

When you are done, push the changes.

### Publications
To add a publication, edit `./data/publications.yml`. Find the appropriate section (e.g. Books, Book Chapters, Journal Papers, etc), and add a new entry under articles. For example:

```
  - title: "Paper Title."
    authors: 'A. Author, T. Huang.'
    venue: 'Conference name'
    year: '2016'
```


## Preview the page

After you change the files, you can use the following command to view the page locally:

``` 
jekyll s
```
Then, enter your browser with `127.0.0.1:4000`. 

When you are done, push the changes.
