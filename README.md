# Stanford Daily Tech Practicum website

This is the website for the Stanford Daily Tech Practicum course for Spring 2019. Site is live at https://tech.stanforddaily.com. Contributions welcome!


## Development setup

To work on the website locally a using Jekyll, you need to:
####1. Setup Jekyll Development Environment
  1. Install [Ruby](http://www.ruby-lang.org/en/downloads/)

  1. Install [Ruby Gems](http://rubygems.org/)

  1. Install [Jekyll] using the following command:
```sh
gem install jekyll
```

  1. Install the latest version of [redcarpet](https://github.com/vmg/redcarpet) the Markdown to (X)HTML converter
```sh
gem install redcarpet
```

  1. Install [Pygments] for code syntax highlighting
```sh
pip install pygments.rb
```

Note for system wide installs, you need to use `sudo` for these commands if you are on a linux system.

####2. Clone the Website Repository
```bash
git clone https://github.com/TheStanfordDaily/tech-practicum.git
cd tech-practicum
```

####3. Launch Jekyll
The easiest way to activly work with Jykell is to have the Jykell builder and web server watch the repository for any changes. You can achieve that by
```bash
jekyll build --watch
jekyll serve --watch
```

Then, point your web browser to [http://localhost:4000](http://localhost:4000) to see a live rendering of the website.

#### Notes & Hints
##### Generating CSS for Syntax Highliting
You may need to update the css generating to perform syntax highliting for code blocks. To do that, you run [Pygments]
```sh
pygmentize -S default -f html > css/pygments.css
```


[Jekyll]: http://jekyllrb.com/ "Jekyll Blog Aware Static Website Generator"
[Pygments]: http://pygments.org/ "Python Pygments"
