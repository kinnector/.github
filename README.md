# Kinnector GitHub Organization Defaults

This repository holds organization-wide configurations, workflow templates, community health files, and profile assets for the `kinnector` GitHub organization.

---

## Why this exists

Maintaining consistent issue templates, pull request workflows, and profile homepages across multiple repositories in an organization requires a central configuration repository that GitHub automatically references as a fallback.

---

## Repository Structure

* **`profile/`**: Contains the organization profile README (`profile/README.md`) displayed on the main `kinnector` organization homepage.
* **`workflow-templates/`**: Shared GitHub Action workflow definitions.

---

## Managing Defaults

To register organization-wide defaults, place them in this repository following standard GitHub layout paths:
* **Issue Templates**: `.github/ISSUE_TEMPLATE/`
* **Pull Request Template**: `.github/pull_request_template.md`
* **Workflow Templates**: `.github/workflow-templates/`