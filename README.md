# Reproduction for `Rails/EnumSyntax` issue

This repository was spun up using the command `rails new <name> --devcontainer`. Only the following files were added:

- `app/models/enum.rb`
- `lib/enum_lib.rb`

To reproduce the issue, follow these steps:

```sh
git clone https://github.com/Splines/repro-rubocop-enum-syntax.git

# This should give 1 offenses
bin/rubocop app/models/enum.rb

# This should also give 1 offenses, since the file content is the same as enum.rb
# However, it yields 0 offenses.
bin/rubocop lib/enum_lib.rb
```
