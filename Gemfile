# frozen_string_literal: true

source "https://rubygems.org"

# https://andycroll.com/ruby/read-ruby-version-in-your-gemfile/
ruby File.read(".ruby-version").strip

git_source(:github) {|repo_name| "https://github.com/#{repo_name}" }

gem "jekyll", "~> 4.1"
gem "liquid-c"
gem "jekyll-last-modified-at", git: "https://github.com/maximevaillancourt/jekyll-last-modified-at", branch: "add-support-for-files-in-git-submodules"

gem "nokogiri"
# gem "jekyll-commonmark-ghpages"
