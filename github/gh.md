Confirm you're now using the correct account
```
gh auth status
```

If you need to switch between accounts often, you can use gh profiles:

```
gh auth login --profile work
gh auth login --profile personal

```

Then switch like this:

```
gh auth status --profile personal
gh auth status --profile work
```

Or set the default profile per repo with:

```
gh config set profile work
```
