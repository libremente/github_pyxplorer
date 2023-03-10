# GitHub pyxplorer

Simple interactive program to explore a GitHub organization and 
extract some information.
It uses GitHub's API. 

# Options

### -d, --dry-run, Dry run option

This option allows to perform a dry-run, nothing will be persisted.
A Github token is needed in order to avoid GH API's rate limit. 
Pass the organization name after the `-d`. 

> NOTE: GH heuristics catches if a repo has a license 
by checking the `LICENSE.md` or `LICENSE` files. Here we are digging a bit 
deeper in order to see if there are other files that "may" contain licensing
info in the root of the repo.


```bash
export GH_TOKEN=<your_github_token>
python3 crawler.py -d <organization_name>
```

#### Output

```bash
repo_name,license,primary_language
```

#### Testing

Run

```bash
python3 -m unittest tests.py
```

# License

MIT License, see [LICENSE](LICENSE.md)