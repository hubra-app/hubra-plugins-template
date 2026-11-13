# Example

## Unreleased

- CI: the step "Personal data goes with the member" in `plugin.yml` fails
  when a table keeps personal data core doesn't export or delete with the
  member (e-mail, phone, address, IBAN … in a row that outlives the member,
  or a member id without a foreign key) and the plugin offers no
  `privacy_contracts()`, or when an offer names a missing handler. A
  `# privacy: <reason>` comment on the column exempts it. A plugin gets it
  when its `release.yml` pin moves past this commit.
- CI: an `audit` job in `plugin.yml` checks for known vulnerabilities with
  pip-audit (Hubra's backend lock and the plugin's own `requirements*.txt`)
  and npm audit (runtime packages of Hubra's frontend, which are bundled into
  `plugin.js`, and the plugin's own `frontend/package-lock.json`, high and
  critical). A plugin gets it when its `release.yml` pin moves past this commit.
- `role_defaults`: Mitglied sees the notice board, Vorstand edits it,
  Aktuar/in has everything when a club first switches it on. Needs Hubra
  0.2.5 or later (standard roles and module access, hubra#275).
- Contracts: a query, an event and a dashboard widget other plugins and
  the dashboards use (`hubra_example/contracts.py`), with tests. Needs Hubra
  with contracts (hubra#231) and contract widgets (hubra#234).

## 0.1.0

First version of the template: a notice board with one table, an API, a
club-app screen, a setting and tests.
