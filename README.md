# XZ Backdoor Github Analysis

This repo contains a simple Jupyter Notebook that allows you to query Github's GraphQL API for a user's commit history. The particular focus of this repo is recent XZ supply chain compromise. The primary user of interest was [JiaT75](https://github.com/JiaT75).

The data currently being used in this visualization was captured at around 7:00PM EST on 2024/03/29. Since Github has removed the repository, if you refetch the data now, you will get different results.

There are plenty of plausable explanations for why the commits of interest occurred at such a strange time. Keep in mind that, by itself, none of this is a damning piece of evidence by any means. It is simply an interesting observation. I'm not making any claims about what this could mean, so any interpretation/speculation is an exercise for the reader.

**Important caveat:** please **do not** start accusing random OSS authors of being malicious actors without **credible** evidence. It is already a thankless job and there is no need to make their lives harder. <3

## Setup

The only dependencies for this are `matplotlib` and `pandas`. A [`poetry`](https://python-poetry.org/) env is included if you want it.

You might need to add jupyter as a dependency, not sure.

```bash
poetry add -D jupyter
```

You can run the notebook using `poetry` with:

```bash
poetry run jupyter notebook
```

## Repo Structure

- `Analysis.ipynb` is the Jupyter Notebook for recreating results.
- `/data` contains the unaltered results from [Jai's] commit history.
- `/images` is where any newly generated plots will be saved.

## References

I've included some relevant links that might be helpful for context:

- [CISA's Advisory](https://www.cisa.gov/news-events/alerts/2024/03/29/reported-supply-chain-compromise-affecting-xz-utils-data-compression-library-cve-2024-3094)
- [Original Openwall Notification](https://www.openwall.com/lists/oss-security/2024/03/29/4)
- [FAQ on the xz-utils backdoor](https://gist.github.com/thesamesam/223949d5a074ebc3dce9ee78baad9e27)
