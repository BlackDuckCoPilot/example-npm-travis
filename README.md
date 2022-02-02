# Black Duck CoPilot npm/Travis CI Example

[![Build Status](https://travis-ci.org/BlackDuckCoPilot/example-npm-travis.svg?branch=master)](https://travis-ci.org/BlackDuckCoPilot/example-npm-travis) [![Black Duck Security Risk](https://copilot.blackducksoftware.com/github/repos/BlackDuckCoPilot/example-npm-travis/branches/test/badge-risk.svg)](https://copilot.blackducksoftware.com/github/repos/BlackDuckCoPilot/example-npm-travis/branches/test)

Shows a working setup for using Synopsys CoPilot to analyze the risk of project dependencies

## Travis CI Setup
The `.travis.yml` file has been modified to upload generated dependency data to CoPilot:

```yaml
after_success:
  - bash <(curl -s https://copilot.blackducksoftware.com/ci/travis/scripts/upload)
```
