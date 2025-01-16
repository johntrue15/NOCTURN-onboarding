setup-config.yml

on: pull_request (to main)
Checks if config.ini was modified, ensures required fields are present.
On success, merges PR or requests review.
On merge, updates the README to Step 3.
windows-path.yml

on: push (to main), with a path filter for windows_path.txt or config.ini.
If path is valid, updates README to Step 4.
device-flow-authorization.yml

on: push or on: repository_dispatch (if Pi calls a webhook on successful authorization).
Confirms the Pi’s device flow is complete and merges a “device-activated” branch.
Updates README to Step 5.
pca-detected.yml

on: push (to main), checks references to .pca or other metadata.
If .pca is present, triggers a GitHub Release with the config metadata.
Updates README to final “Complete” status.
