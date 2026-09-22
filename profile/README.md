<p align="center">
  <img src="https://raw.githubusercontent.com/dosvak/.github/master/profile/dosvak-logo.png" width="160" alt="Dosvak">
</p>

<h1 align="center">Dosvak</h1>

<p align="center">
  Open-source tooling for <b>IBM Business Automation Workflow</b> (BAW), <b>IBM BPM</b> and <b>IBM Cloud Pak for Business Automation</b> (CP4BA):
  ready-to-import process applications, toolkits, analyzers and utilities for people who build and run BAW.
</p>

<p align="center">
  <a href="https://dosvak.com">dosvak.com</a> ·
  <a href="https://bpm.tips">bpm.tips</a> (questions and answers) ·
  <a href="https://twxca.com">twxca.com</a> (TWX Code Analyzer live demo)
</p>

---

Dosvak LLC is an IBM Business Partner (Silver, IBM Partner Plus) building and running IBM BPM / BAW / CP4BA solutions.
The products below are the tools we use ourselves, published as open source under the
**Apache License 2.0** (free to use, modify and redistribute, attribution required). Every process application is built from
out-of-the-box building blocks only - System Data, UI Toolkit, client-side human services, service flows - so it imports on
traditional BAW (verified on IBM BPM 8.6.2 / BAW 20.0.0.1) and on CP4BA (Workflow Authoring / Business Automation Studio, verified on 25.0.1).
Packages for both targets are in every repository (`packages/` and `packages/cp4ba/`) and attached to the releases.

## Products

| Repository | What it is | Target |
|---|---|---|
| [baw-mcp](https://github.com/dosvak/baw-mcp) | **BAW Knowledge MCP server** - IBM BAW / CP4BA authoring knowledge for AI agents (IBM Bob, Claude Code, Cursor, any MCP client): authoring method and checklist, verified engine facts, REST API catalogue and map, TWX structure, coach guidelines, CP4BA differences, install runbooks, app designs and the 156 analyzer rules - **public endpoint: `https://bawmcp.dosvak.com/mcp`**, no account | BAW, CP4BA |
| [generic-ui-toolkit](https://github.com/dosvak/generic-ui-toolkit) | 47 coach view controls (layouts, navigation, charts and maps, viewers and exports, inputs, display and logic, composites) without commercial libraries, plus a showcase app with a demo page per control | BAW, CP4BA |
| [twx-code-analyzer](https://github.com/dosvak/twx-code-analyzer) | static analysis of `.twx` exports: 156 rules, findings ranked by impact, toolkit usage, diagrams, TWX search, snapshot comparison; desktop app, CLI, embeddable Java facade, WAR for a shared server, and a BAW process app | any BAW export; app for BAW |
| [operations-cp4ba](https://github.com/dosvak/operations-cp4ba) | operations dashboard with 31 administration tools (instances, tokens, timers, tasks, event manager, containers, snapshots, deployment, health, users) on the Process, Operations and federated REST APIs through a reusable REST Framework service; Operations REST and Operations for traditional servers | CP4BA, BAW |
| [process-tools-rest](https://github.com/dosvak/process-tools-rest) | the process administration tools rebuilt the "vanilla" way - business objects, service flows, OOB controls, no JavaScript library - plus Bulk Move Tokens | BAW, CP4BA |
| [failed-instance-triage](https://github.com/dosvak/failed-instance-triage) | failed instances grouped by error signature: retry / terminate / delete per cause, runtime errors, failures per day | BAW, CP4BA |
| [instance-migration-console](https://github.com/dosvak/instance-migration-console) | snapshots with instance counts, orphan-token check and instance migration between snapshots over the Operations REST API | BAW, CP4BA |
| [container-version-manager](https://github.com/dosvak/container-version-manager) | process apps, toolkits, snapshots, environment variables and cleanup over the Operations REST API - no wsadmin | BAW, CP4BA |
| [test-data-generator](https://github.com/dosvak/test-data-generator) | four tiny processes and a dashboard that creates instances and tasks in every state, for testing operations tooling | BAW, CP4BA |
| [headless-process-portal](https://github.com/dosvak/headless-process-portal) | Angular replacement of Process Portal on the engine REST API only (task lists, headless task forms, dashboards) - **live demo: https://portaldemo.dosvak.com** (demo accounts on the login page), with a sample process application | BAW, CP4BA |
| [baw-json](https://github.com/dosvak/baw-json) | server-side JavaScript library converting business objects to JSON and back for every BAW type, shipped as a toolkit, with the test app that validated it against real REST payloads | BAW, CP4BA |
| [baw-operations-utilities](https://github.com/dosvak/baw-operations-utilities) | task counts per process application (REST script, SQL, JavaScript API and a process app), closed-task and unnamed-snapshot cleanup for CP4BA | BAW, CP4BA |
| [sla-deadline-monitor](https://github.com/dosvak/sla-deadline-monitor) | overdue and soon-due tasks across applications in lateness buckets, reassignment to a user or group, CSV | BAW, CP4BA |
| [team-workload-balancer](https://github.com/dosvak/team-workload-balancer) | open tasks per person and team with overdue counts, the tasks of a person, reassign or return to the team | BAW, CP4BA |
| [team-audit](https://github.com/dosvak/team-audit) | teams and members of every installed application, empty and single-member teams flagged, exposed items, user membership lookup | BAW, CP4BA |
| [process-smoke-test-runner](https://github.com/dosvak/process-smoke-test-runner) | JSON test cases started over REST, polled to the expected state, pass / fail report, re-check, cleanup - regression checks inside the server | BAW, CP4BA |
| [instance-timeline](https://github.com/dosvak/instance-timeline) | process instances of a period on a Gantt-style timeline grouped by application, overdue and at-risk colouring | BAW, CP4BA |
| [orphan-zombie-cleaner](https://github.com/dosvak/orphan-zombie-cleaner) | idle instances, instances of inactive or not installed snapshots, overdue tasks nobody holds, old finished instances - bulk terminate / delete | BAW, CP4BA |
| [environment-variable-diff](https://github.com/dosvak/environment-variable-diff) | environment variable values of two snapshots or two servers side by side over the Operations REST API | BAW 20+, CP4BA |
| [deployment-runbook-generator](https://github.com/dosvak/deployment-runbook-generator) | a Markdown deployment checklist generated from an installed snapshot: package facts, environment variables, team bindings, exposed items, activation steps | BAW 20+, CP4BA |
| [business-data-search](https://github.com/dosvak/business-data-search) | cross-application business data search on the registered aliases, by instance or by task, with CSV export | BAW, CP4BA |
| [notification-manager](https://github.com/dosvak/notification-manager) | per-user subscriptions to application events (new tasks, team tasks, overdue tasks, failed / completed instances) with an e-mail digest; subscriptions stored as shared saved searches | BAW, CP4BA |
| [process-performance](https://github.com/dosvak/process-performance) | step durations (average, median, P95 per activity), instance durations, throughput per day with a chart, observed variants | BAW, CP4BA |
| [role-inbox](https://github.com/dosvak/role-inbox) | the inbox of one role across every application | BAW, CP4BA |
| [event-manager-monitor](https://github.com/dosvak/event-manager-monitor) | event manager tasks (timers, UCA runs, messages) with pause / resume, delete and replay, schedulers, and the scheduled undercover agents of every snapshot | BAW, CP4BA |
| [snapshot-lifecycle](https://github.com/dosvak/snapshot-lifecycle) | toolkit dependency tree of every application snapshot and a rollback advisor per container (running instances, open tasks, flags, advice) | BAW, CP4BA |
| [bpm.tips](https://github.com/dosvak/bpm.tips) | the community Q&A site for IBM BPM / BAW / CP4BA | - |

The fourteen applications from **sla-deadline-monitor** to **snapshot-lifecycle** are the *kit apps*: each is generated from a ~200-line
Python program on the twxkit generator (standard library only, no base export), verified on the labs, and re-buildable with your own
defaults through the [BAW Knowledge MCP server](https://github.com/dosvak/baw-mcp) (`get_package`, `get_tool('build_<acr>.py')`,
`get_topic('howto-kit-utility-app-recipes')`). Every repository carries the package, the design document and the recipe collection.

## For AI agents

Add `{ "mcpServers": { "baw-knowledge": { "url": "https://bawmcp.dosvak.com/mcp" } } }` to your MCP client (IBM Bob `~/.bob/settings/mcp.json`,
Claude Code `claude mcp add --transport http baw-knowledge https://bawmcp.dosvak.com/mcp`, Cursor / VS Code settings) and your agent can search
and read the knowledge behind every project on this page - see [baw-mcp](https://github.com/dosvak/baw-mcp) for the tools and terms.

## Using the packages

1. Download the `.twx` from the repository (`packages/` for traditional BAW, `packages/cp4ba/` for Cloud Pak) or from its releases.
2. Traditional BAW: Process Center console > *Import Process App*. CP4BA: Business Automation Studio > *Business automations* > *Import*.
3. Set the application's environment variables for your server (REST base URL, technical user, context paths - documented in each README), expose the dashboard to a team, run.

The applications never ship credentials: the technical user's password is empty in every package and must be set after the import.

## How we work

* **Out-of-the-box only.** No third-party toolkits, no custom Java where a service flow will do, no heritage coaches. What we publish should still import on the next version.
* **REST first.** Administration tools talk to the engine through its documented REST APIs (Process REST v1 / v2, Operations REST, federated REST), never through the database when an API exists.
* **Verified, with the evidence in the repository.** Automated functional sweeps and design-time sweeps run on traditional BAW and on CP4BA; the reports are in `docs/` of each product.
* **Attribution, not restriction.** Apache-2.0 everywhere; keep the LICENSE and NOTICE files with your copies and you are done.

Issues and pull requests are welcome in each repository. For consulting, embedded deliveries or support contracts: [dosvak.com](https://dosvak.com).

---

<sub>IBM, IBM Business Automation Workflow, IBM Business Process Manager and IBM Cloud Pak are trademarks or registered trademarks of
International Business Machines Corporation. Dosvak LLC publishes these projects as an IBM Business Partner; they are not affiliated
with, endorsed by or supported by IBM.</sub>
