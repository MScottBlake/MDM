# Scripts
Some scripts I find useful. Maybe you will, too.

## [set-proxyVariables.zsh](set-proxyVariables.zsh)

Proxies are rarely fun to deal with, especially when pairing them high-security setups to limit admin-level permissions to nearly all aspects of macOS, which prevents users from many self-help options.
Because of this, I set out to script a way to set your proxy information by script using an MDM, in this case Jamf.
My goals were:
1) Flexible.
- Needs to be easily changeable. In case hosts or URLs change, being able to quikcly modify only a parameter and not the core script makes changes faster and more predictable.
2) Easy to deploy.
- Deploying via MDM is the easiest and most reliable option. Jamf's script runner is great and allows for parameters to be labeled and modified within a policy without modifying the script directly.
4) Non-invasive.
- Will not interrupt ay existing connections (open Terminal windows). Also, if an OS update clears out the system shell profile, the settings won't throw errors when opening a Terminal.
5) Easy to remove (or ensure missing info didn't break connections).
- Avoid having to remove lines from a system shell profile at all costs. Instead, only *add* a one-liner to check for a settings file and source it if exists.

Check the comment block in the script for params.
I cannot share screenshots at this time, sorry.

## [Create-JiraIssuesForClinics.ps1](Create-JiraIssuesForClinics.ps1)

This was a very specific project to create a massive amount of Jira issues for hundreds of physical sites and leverage Google Maps' API to put clickable map links in the issues for use by local service techs.
