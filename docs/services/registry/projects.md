# Projects

## Projects within EIDF

Every EIDF project can request that a project with the ECIR is created for them. This project will be private to the project.

### Project Quota

Each project will be given 50 GiB of storage for images to use.

Requests for increase in quota should be submitted via the [EIDF Portal](https://portal.eidf.ac.uk).

### Naming

The default project name for each project will be their EIDF project number in the form:

```bash
eidfXXX
```

### Vulnerability Level Tolerance

The default position of the ECIR is that all images can be deployed onto services, if a project would prefer to have a restriction on the vulnerabilities they are willing to tolerate in their projects, a request can be made to helpdesk to enforce a maximum level of vulnerability tolerance.

Vulnerabilities are ranked:

* Critical
* High
* Medium
* Low

Vulnerability scanning is provided via trivy, more information about severity levels can be found on the [trivy documentation](https://trivy.dev/latest/docs/scanner/vulnerability/#severity-selection).

### Permissions

ECIR users have the project maintainer role permissions.

This allows users to create and delete repositories in a project, to push and pull images from a project, initiate vulnerability and SBOM scans, view the results of scans, edit the labels available to a project and work on the policy rules for a project.

Project maintainers do not have the permissions to create new projects, edit project configuration or delete projects.
