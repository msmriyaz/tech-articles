### To Build the existing site:
bundle exec jekyll serve
bundle exec jekyll build --watch

### Before Checkin the code
Remove-Item -Recurse -Force .jekyll-cache
bundle exec jekyll clean

### To build again
bundle exec jekyll build --watch