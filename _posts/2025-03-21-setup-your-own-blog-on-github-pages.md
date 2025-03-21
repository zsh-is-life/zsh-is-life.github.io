# Quick Crash Course on Setting Up on your own Blog on Github Pages

This guide will make use of Jekyll to generate your own blog. There are alternatives to Jekyll, like Hugo, Hexo etc.

### Steps

1. You'll need a Github account (obviously).

2. Make a public repository with the name `<your-username>.github.io`. This is necessary. Your website will eventually point to `https://<your-username>.github.io`. You can change your domain name, later.

3. Throw in a simple `README.md` file in your repository.

4. `git clone` your repository to your machine.

5. Now, it is time to setup Jekyll on your machine. (

   [Jekyll Installation Guide]: https://jekyllrb.com/docs/installation/	"Jekyll Installation Guide"

   ). Follow the guide, according to the OS of your machine. Your should now have Jekyll on your machine.

6. `cd` into your repository and run `jekyll new --skip-bundle .` Open your `Gemfile` in a text editor, say `vim` or `nano`. Remove the line that says `gemfile "jekyll"` add a new line `gem "github-pages", "~> GITHUB-PAGES-VERSION", group: :jekyll_plugins` where `GITHUB-PAGES-VERSION` corresponds to the version number corresponding to `github-pages` here https://pages.github.com/versions/. Save and close your `Gemfile`.

7. Run `bundle install`. Add `Gemfile.lock` to the `.gitignore` file, to make `git` avoid that `.lock` file.

8. Add your domain and url to the `_config.yml` file.

9. Run `git add.`, `git commit -m "init"`, `git push -u origin main` (Assuming the remote repo's branch you're pushing to is called `main`). `origin` should be already defined because of the `git clone` command you ran earlier.

   1. You may run into problems when running the `git push` command. Github does not permit plain passwords anymore. You'll have to setup a Personal Access Token (https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens).

10. Check out the `https://github.com/your-username/your-username.github.io/actions` URL for any build errors. (Github attempts to parse the `markdown` and config files present and uses Jekyll to generate `html` files that browsers can parse and display)

11. If no issues, feel free to visit `https://<your-username>.github.io` and check out your website.

12. You may change your domain name here `https://github.com/your-username/your-username.github.io/settings/pages`

### Important Resources

1. https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll
2. https://jekyllrb.com/