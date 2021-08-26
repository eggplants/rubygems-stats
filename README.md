# rubygems-stats

- Create a list of Authors from [Rubygems.org](https://rubygems.org)
- Add their twitter account to [List](https://twitter.com/i/lists/1428185251101036545)

## Scripts

- `get_authors`: Retrieve a user with `/profiles/` who has OWNED or PUSHED at least one Gem

  - `gem_authors.txt`: Result

- `get_letters`: Get the number of Pages and Gems by acronym and their total

  - `letters.csv`: Result

- `get_twitter_account`: Get a Twitter account from `gem_authors.txt`

  - `twitters.csv`: Result

- `add_gemdevs_list`: Add accounts listed on `twitters.csv` to [List](https://twitter.com/i/lists/1428185251101036545)

  - `add.log`: Log

- `diff_lists_and_csv`: Compare accounts in `twitters.csv` with registered users in the List

  - `list_members.json`: Acquired List registered user information

- `check_exist`: Confirm the existence of the account listed in `twitters.csv`
  - `deleted.txt`: Accounts that seem to be deleted
  - `protected.txt`: Accounts that seem to be protected
  - `exist.txt`: Accounts that existed and are not on the [List](https://twitter.com/i/lists/1428185251101036545)

## Requirements

- cURL, diff, Jq, [twitter/twurl](https://github.com/twitter/twurl)

```bash
sudo apt install curl diffutils jq
gem install twurl
```

## Stats

- At 2021/08/13
- 167470 Gems, 58314 Users, 4453 Twitter accounts
