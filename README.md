# [GitHub Stats Visualization](https://github.com/jstrieb/github-stats)

<a href="https://github.com/jstrieb/github-stats">

![](https://github.com/ntalbs/github-stats/blob/master/generated/overview.svg)
![](https://github.com/ntalbs/github-stats/blob/master/generated/languages.svg)

</a>

Please visit [the original reop](https://github.com/jstrieb/github-stats) to see the background of the project, how to setup, etc.

## Excluding repos, langs from the stats
To exclude (or ignore) certain repos or langs, you need to add(or update) secrets named `EXCLUDE` (for repos) or `EXCLUDE_LANG` (for languages).

1. Go to Settings > Secrets > Actions or simply click [this](https://github.com/ntalbs/github-stats/settings/secrets/actions).
2. Update (or add if they don't exist) `EXCLUDE` to exclude certain repos, or `EXCLUDE_LANG` to exclude certain languages.

You can't see the values of the secrets once you saved as those are regarded as secrets. 
Actually, `EXCLUDE` and `EXCLUDE_LANG` don't need to be secrets, and it's very inconvenient if you want to update them. 

### Current settings:
```
EXCLUDE=ntalbs/ntalbs.github.io,ntalbs/github-stats
EXCLUDE_LANG=html,stylus,css,ejs
```

### Manually excuting workflow
Currently, the workflow is set to be executed every day at `00:05` am. You can find this schedule setting in [`.github/workflows/main.yml`](
https://github.com/ntalbs/github-stats/blob/master/.github/workflows/main.yml#L10).

If you want to update the stats image immediately, you can manually run the workflow. Go to the [Action Page](https://github.com/ntalbs/github-stats/actions/workflows/main.yml) and click `Run workflow`.
