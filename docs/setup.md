# Setup Instructions

## Mkdocs Setup

1) Signup for github and send your username to Noah or Jimmy.

2) Install python 3 on your computer

3) Install mkdocs

```bash
pip install mkdocs
```

4) Create a folder and open it in vs code for your new docs.

5) Open a terminal in vs code and type in the following command.

```bash
mkdocs new .
```

6) Type in mkdocs serve to see what your docs look like.

7) Go into the mkdocs.yml file and change the Site Name to something about your docs.

```yaml
site_name: How to setup mkdocs
```

8) Add a theme to your mkdocs I like the read docs theme.

```yaml
site_name: How to setup mkdocs
theme: 
    name: readthedocs
```

9) Add highlight js for language highlighting and list the languaes you are planning on documenting.  In this example I did lua, javascript, and python.

```yaml
site_name: How to setup mkdocs
theme: 
    name: readthedocs
    highlightjs: true
    hljs_languages: ['lua', 'javascript', 'python']
```

## Adding Pages

1) Let's a page to our docs.  Create a markdown page called tictactoe.md.  Copy the contents below into the markdown file.

```markdown
# How to build a tic tac toe Game
```

2) Now go to the mkdocs.yml file and add this page to your navigation.

```yaml
site_name: How to setup mkdocs
nav: 
  - MkDocs Class: setup.yml
theme: 
    name: readthedocs
    highlightjs: true
    hljs_languages: ['lua', 'javascript', 'python']
```

3) Now add Some sections to your markdown page.

```markdown
## Demo

## Steps

## Assets
```

4) To add code to your mkdocs do this for syntax highlight.

\`\`\`jasascript

let b = 4;

\`\`\`

## Adding images 

1) Create a folder in your docs called images.

2) Add an image your want to upload there.  I am going to add an image called calculator.png

3) Add your image to the markdown file. The alt text is for people who can not see.

```markdown
![alt text](images/calculator.png)
```

![calculator](images/calculator.png)

## Deploying Mkdocs

1) Commit your repo to github.

2) Run the command mkdocs gh-deploy

3) Go to your github repos settings and scroll down. You should see the url.

## Adding styles and javascript

1) Go to your mkdocs.yml file and add this 

```
extra_javascript:
    - js/ex.js
extra_css:
    - css/style.css
```

2) In your docs folder create js folder and css folder and create the ex.js and style.css.

3) Test the js by adding an alert

4) I like to add this to css so that my docs can take up the full screen.

```css
.wy-nav-content {
    max-width: none;
}
```

## Github  Repo

You can see the code for this here.

