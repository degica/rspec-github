# Rspec::Github
[RSpec](https://rspec.info/) formatter compatible with [GitHub Action](https://github.com/features/actions)'s annotations. It supports multiline errors and will set pending specs as warnings:

![screenshot.png](docs/screenshot.png)

## Installation
Add the gem to your application's `Gemfile` `test` group:
```ruby
group :test do
  gem 'rspec-github', require: false
end
```

And then of course install the gem by executing:
```shell script
bundle install
```

## Usage
You can specify the formatter with a command line argument:
```shell script
rspec --format RSpec::Github::Formatter
```

And to always run it with this formatter, you can set it in the `.rspec` file:
```
# other configuration
--format RSpec::Github::Formatter
```

## Development
After checking out the repo, run `bundle install` to install dependencies. Then, run `rake spec` to run the tests. 
Publishing a new version is handled by the [publish workflow](.github/workflows/publish.yml). This workflow publishes a GitHub release to [rubygems](https://rubygems.org/) with the version defined in the release. 

### Usefull references
- https://help.github.com/en/actions/reference/development-tools-for-github-actions
- https://developer.github.com/apps/quickstart-guides/creating-ci-tests-with-the-checks-api

## License
The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
