# cfpctl-data

Conference deadline data for [cfpctl](https://github.com/yuranqiu/cfpctl).

## Structure

```
*.yaml          # Conference data files (one per CCF category)
full_refresh.py # Script to refresh all data from ccfddl
import_accept_rates.py # Script to import acceptance rates
clean_tbd.py    # Clean TBD entries
clean_no_deadline.py # Clean entries without deadlines
```

## Data Format

Each YAML file contains a list of conferences:

```yaml
- name: NeurIPS
  slug: neurips
  rank:
    ccf: A
    core: A*
  fields: [ai, ml]
  homepage: https://neurips.cc
  verified: true
  accept_rate: "24.5%(5290/21575 25')"
  cycles:
    - name: "2026"
      abstract: "2026-05-04T23:59:59-12:00"
      deadline: "2026-05-06T23:59:59-12:00"
      notification: "2026-09-24"
```

## Contributing

1. Edit the appropriate YAML file
2. Run validation: `cfpctl validate`
3. Submit a PR

## License

MIT
