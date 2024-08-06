# OSCAL Compass Security Policy

This policy describes OSCAL Compass security and disclosure information.

## Reporting a vulnerability

To report a vulnerability, either:

1. Report it on Github directly you can follow the procedure described
   [here](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing/privately-reporting-a-security-vulnerability)
   and:

    - Navigate to the security tab (e.g. `trestle` [security tab](https://github.com/oscal-compass/compliance-trestle/security)) on the repository
    - Click on 'Advisories'
    - Click on 'Report a vulnerability'
    - Detail the issue, see below for some examples of info that might be
      useful including.

2. Send an email to `oscal-compass-oversight@googlegroups.com` detailing the issue and impacted project(s).

## Public Disclosure

Vulnerabilities once fixed will be shared publicly as a Github [security
advisory](https://docs.github.com/en/code-security/security-advisories/repository-security-advisories/about-repository-security-advisories)
and mentioned in the fixed versions' release notes.

## Supported Versions

All OSCAL Compass projects follow [Semantic Versioning](https://semver.org/) terminology and are expressed as x.y.z:
- where x is the major version
- y is the minor version
- and z is the patch version

Security fixes are typically addressed in the main branch and may be backported to one prior minor release depending on severity and feasibility.

## Acknowledgments

Parts of this policy were adapted from the Crossplane [security policy](https://github.com/crossplane/crossplane/blob/master/SECURITY.md)