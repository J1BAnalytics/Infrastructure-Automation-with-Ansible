
### `AnsiblePlaybooks.md`:

```markdown
# Ansible Playbooks for Infrastructure Automation

This document explains the structure, usage, and best practices for creating Ansible playbooks to automate infrastructure tasks.

## Playbook Structure

An Ansible playbook typically consists of:

- **Hosts**: Define target hosts or server groups in the inventory (`hosts`) file.
- **Variables**: Store variables used in playbooks in separate files (`vars/*.yml`).
- **Tasks**: Define tasks to be executed on target hosts. Tasks use Ansible modules to perform actions.
- **Handlers**: Define handlers to respond to changes triggered by tasks.

## Creating Playbooks

### Basic Structure

A basic playbook structure includes:

```yaml
---
- name: Playbook Name
  hosts: app_servers
  become: true
  tasks:
    - name: Task Name
      <module_name>:
        <module_options>
