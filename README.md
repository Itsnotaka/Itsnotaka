```bash
Hey, I'm Aka 👋
```
[![Discord Presence](https://lanyard-profile-readme.vercel.app/api/365733917090906113)](https://discord.com/users/365733917090906113)

[![wakatime](https://wakatime.com/badge/user/86365d17-8c9f-4063-8547-f42d617ca55b.svg)](https://wakatime.com/@86365d17-8c9f-4063-8547-f42d617ca55b)

# Visit https://github.com/lowlighter/metrics/blob/master/action.yml for full reference
name: Metrics
on:
  # Schedule updates (each hour)
  schedule: [{cron: "0 * * * *"}]
  # Lines below let you run workflow manually and on each commit
  workflow_dispatch:
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          # Your GitHub token
          # The following scopes are required:
          #  - public_access (default scope)
          #  - public_repo
          # The following additional scopes may be required:
          #  - read:org  (for organization related metrics)
          #  - read:user (for user related data)
          #  - repo      (optional, if you want to include private repositories)
          token: ${{ secrets.METRICS_TOKEN }}

          # Options
          user: itsnotaka
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: America/New_York
          plugin_activity: yes
          plugin_activity_days: 14
          plugin_activity_filter: all
          plugin_activity_limit: 5
          plugin_activity_load: 300
          plugin_activity_visibility: all
          plugin_introduction: yes
          plugin_introduction_title: yes
          plugin_isocalendar: yes
          plugin_isocalendar_duration: half-year
          plugin_languages: yes
          plugin_languages_analysis_timeout: 15
          plugin_languages_categories: markup, programming
          plugin_languages_colors: github
          plugin_languages_ignored: html, css
          plugin_languages_limit: 8
          plugin_languages_recent_categories: markup, programming
          plugin_languages_recent_days: 14
          plugin_languages_recent_load: 300
          plugin_languages_sections: most-used
          plugin_languages_threshold: 0%
          plugin_projects: yes
          plugin_projects_limit: 4
          repositories: 5
          repositories_batch: 5
          
# 📫 Contact
To contact me quickly and easily, [DM me on Twitter](https://twitter.com/gem8160).

If it's something more business related, email me: inquiries@kakaka.dev
