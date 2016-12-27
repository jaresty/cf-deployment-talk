# Core values
Simple
Open
Repeatable

# 1.0 pains
- manifests are too long (x simple)
- manifests are not easily resuable (x open x reusable)
- manifests are too deep (stubs) (x simple)
- manifests are too private (creds) (x open)
- manifests are too hard to make (creds, flags, ...)
- manifests are too inflexible, and thus brittle (x simple x Repeatable)
- manifests are too hard to upgrade
- manifest knowledge buried in many places (like manifest generation scripts, for example), so even experts have trouble

# Bosh 2.0 features
- Cloud config extracts details of particular infrastructure
  simpler and more repeatable
- var store extracts credentials
  - open (extract) -simple (fewer lines) -repeatable (generation)
- Links allow jobs to share their configuration (when configured via bosh like IP addresses or via manifests) with other jobs
  - simple (omit noise) - repeatable (ip addresses) -open (clear where values are)
- ops files
  - repeatable (eliminates stubs)

## Dubious Decisions
These are things that we are not certain about long term, and thus might change in the future.
- no global properties
- our ops file structure

# Bosh 2.0 Transitions
resource pools => vm types
cloud properties => cloud config
jobs => instance groups
stubs => var store and ops files
spiff + bosh => just bosh

# blah blah blah -- notes that may be dropped
- Used cloud config to extract details of our particular infrastructures and environments, allowing us to freely share our base CF deployment manifest
- Used BOSH's var store feature to automagically generate credentials and certificates to configure all jobs without having to generate a single password by hand
- Used and designed for BOSH links to allow BOSH to handle configuring and 

