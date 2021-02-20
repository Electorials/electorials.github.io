[electorials.com](https://electorials.github.io)

## To run the site locally...

Steps have to be done on a terminal.

1. In any order:
 
   - Follow the [Jekyll installation instructions for your operating system](https://jekyllrb.com/docs/installation/).

   - Clone the repository to your computer on a directory of your choice, either through downloading the source code from the repo's page and extracting the archive, or `git clone https://github.com/electorials/electorials.github.io.git`.

2. Navigate to the site directory.
    Example: `cd /directory/of/choice/electorials.github.io`
    
3. This step might be necessary. Run `bundle exec jekyll serve` to build and run the site locally. Append `--trace` to see where any errors are occurring.

4. Run `bundle install` to install the required Ruby gems for Jekyll onto your system.

5. Run `bundle update` to update any ruby gems the site uses. Gems and their versions are listed in the Gemfile.lock file.
    What is listed in the Gemfile.lock file when cloning may be out of date. It's best to make sure the gems are up-to-date.

    You might have to run `bundle install` and then `bundle updte` if the gems don't update; the gems installed on your system might be out of date and the new versions for the site probably look for gems installed on your system.

6. Since all gems are updated, instead of running `bundle exec jekyll serve`, you can run `jekyll serve` as a kind of shortcut. You can go further with running `jekyll s t` (the `t` from `--trace`). Refer to the Jekyll help from `jekyll -h`.

The explanations may not be 100% accurate, but hopefully they explain why the order is the way it is.

Refer to these two links for more info about Bundler.
- https://bundler.io/rationale.html
- https://thoughtbot.com/blog/but-i-dont-want-to-bundle-exec
