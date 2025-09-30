# Application Install & Service Validation – Ansible Exercise

## Scenario
Your team needs to automate the setup of an application on a Linux server. The application should be installed in a specific directory, started as a service, and then verified to ensure it is running correctly. The playbook will be run against one or more EC2 instances in AWS.

---

## Requirements
Your playbook should:

1. **Directory Setup**  
   - Create a directory at `/opt/myapp` (or a directory of your choice, parameterized).

2. **Application Installation**  
   - Install an application package (for this exercise, you can assume **nginx** or another service that can be tested easily).

3. **Service Management**  
   - Start and enable the service so it runs on boot.

4. **Validation**  
   - Verify the service is up by:
     - Waiting for the appropriate port to be open (e.g., port 80 for nginx).
     - Performing a health check (e.g., making an HTTP request to confirm the service responds).

---

## Guidelines
- Make the playbook **idempotent** – running it multiple times should not break anything.
- Make it **reusable** – use variables where appropriate.
- Keep it **readable** – structure clearly with comments and proper task names.

---

## What We’re Looking For
- Understanding of basic Ansible modules
- Ability to validate that an application is actually working, not just installed.
- Clean coding practices: variables, readability, and structure.

---

## Need Help?

Links to documentation for modules to use:
- [Package](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/package_module.html)
- [Wait For](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/wait_for_module.html)
- [File](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/file_module.html)
- [Service](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/service_module.html)
- [Uri](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/uri_module.html)
