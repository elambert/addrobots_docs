## Contribute

AddRobots docs use <a href="https://http://www.mkdocs.org/">mkdocs</a> and committed it all to github. This setup not only generates nice-looking, searchable documentation, it makes it possible to share/fork it so that AddRobots can be a community effort.

The mkdocs system is a self-contained, Python-based documentation tool that uses Twitter Bootstrap and scripting to generate high-quality HTML-based documentation using simple markdown files. The cool thing about mkdocs is that the repo is both the documentation set and place to generate the static, production site. The top-level mkdocs.yml file shows the documentation tree structure and configurations. If you edit this file, it will be pretty easy to see what markdown (*.md) files you need to edit in order to change the docs you want changed.

## Installing Python and mkdocs.

Please see the mkdocs website to see how to install Python and the mkdocs tools. It's pretty simple and easy to do this, but it's out-of-scope to explain that here.

## Editing the docs

From a terminal session change to the top-level directory

        >cd ~/git/addrobots_docs
        >mkdocs serve

Now from your browser go to the URL: <a href="http://http://127.0.0.1:8000">http://127.0.0.1:8000</a>

As you edit the markdown files, mkdocs automatically updates the website in realtime so that you can review your changes.

## Generating the Static Documentation Website

Once you've completed all of your edits, you need to generate the static site (not committed to git because "./site" is in .gitignore).

        >cd ~/git/addrobots_docs
        >mkdocs build

This will generate a static documentation site in the directory ~/git/addrobots_docs/site. You can validate the site by killing the "mkdocs serve" process and starting a simple Python=-based web server in that directory:

        >cd ~/git/addrobots_docs/site
        >python -m SimpleHTTPServer 8000

Now from your browser go to the URL: <a href="http://http://127.0.0.1:8000">http://127.0.0.1:8000</a>

## Commit the Static Site to Github Project Pages ("gh-pages")

        >cd ~/git/addrobots_docs
        >mkdocs gh-deploy --clean

This command will generate the static site and push it to the gh-pages branch so that it shows up as a searchable, shred website (on github). The url will be <a href="https://your_github_id.github.io/addrobots_docs/">https://your_github_id.github.io/addrobots_docs/</a>.