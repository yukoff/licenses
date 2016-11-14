# Most used licenses

This is just a collection of mostly used licenses in open-source projects. Actually no need to keep
this - GitHub has amazing [API](https://developer.github.com/v3/licenses/) to get licenses. Under
the hood it uses the open source Ruby Gem [Licensee](https://github.com/benbalter/licensee) to
attempt to identity the project's license.

The Licenses API is currently available for developers to preview. To access the API during the
preview period, a custom media type in the `Accept` header must be provided:
```
application/vnd.github.drax-preview+json
```

For example:
```
curl -H 'Accept: application/vnd.github.drax-preview+json' https://api.github.com/licenses/bsd-3-clause
```

# Some use cases

## List all licenses ([documentation](https://developer.github.com/v3/licenses/#list-all-licenses))

`GET /licenses`

Example:
```
curl -H 'Accept: application/vnd.github.drax-preview+json' https://api.github.com/licenses
```

## Get an individual license ([documentation](https://developer.github.com/v3/licenses/#get-an-individual-license))

`GET /licenses/:license`

Example:
```
curl -H 'Accept: application/vnd.github.drax-preview+json' https://api.github.com/licenses/bsd-3-clause
```
