# Ansible Role: ansible-role-k8s-homelab-setup 🏡

An Ansible role to set up a Kubernetes homelab environment on an Ubuntu server. This role deploys and configures a Kubernetes cluster in either standalone or high-availability mode. It also deploys ArgoCD, a monitoring solution with graph visualizations, alerts to Slack when issues arise, and allows you to deploy a list of apps with their configurations.

## Requirements 📋

- Ubuntu Server 18.04+ or Ubuntu-based distribution.
- Ansible 2.9+ installed on the control machine.
- SSH access to the target server.
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/) installed on the control machine.
- A Slack workspace for receiving alerts (optional).

## Role Variables 🎛️

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
k8s_deploy_mode: "standalone" # "standalone" or "ha" for high availability
k8s_apps: [] # A list of apps to deploy with their configurations
argo_cd_version: "v2.2.2"
monitoring_solution: "prometheus"
alert_manager_slack_webhook_url: ""
cloudflare_api_key: ""
cloudflare_email: ""
```

## Dependencies 🧩

None.

## Example Playbook 📘

```yaml
- hosts: k8s-homelab
  roles:
    - role: ansible-role-k8s-homelab-setup
      k8s_deploy_mode: "standalone"
      k8s_apps:
        - name: "home-assistant"
          config: "/path/to/home-assistant/config.yaml"
      cloudflare_api_key: "your_cloudflare_api_key"
      cloudflare_email: "your_email@example.com"
      alert_manager_slack_webhook_url: "https://hooks.slack.com/services/XXXX/YYYY/ZZZZ"
```

## Adding Apps 🚀

To add apps to your Kubernetes homelab environment, add them to the `k8s_apps` variable in your playbook:

```yaml
k8s_apps:
  - name: "app-name"
    config: "/path/to/app-config.yaml"
```

## Molecule Testing 🧪

To run Molecule tests, first, install Molecule and its dependencies:

```bash
pip install molecule[docker,ansible]
```

Then, navigate to the role directory and run the tests:

```bash
molecule test
```

## Troubleshooting Guide 🔧

If you encounter any issues while using this role, please check the Troubleshooting Guide for common problems and solutions.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

We greatly appreciate any contributions to this project. Your help and expertise can make this Ansible role even better. Here's how you can contribute:

1. **Report issues**: If you find any issues or have suggestions for improvements, please [open an issue](https://github.com/zifamathebula/ansible-role-k8s-homelab-setup/issues) on the GitHub repository. Be sure to include a detailed description and any relevant information to help reproduce or understand the issue.

2. **Submit pull requests**: If you have implemented a new feature or fixed a bug, feel free to submit a pull request. Before submitting, please make sure your changes follow the project's coding style and guidelines. Include a description of your changes, any relevant issue numbers, and a summary of testing performed.

3. **Improve documentation**: Help improve the documentation by fixing typos, clarifying instructions, or adding more examples. Submit your changes as a pull request for review.

4. **Share your experiences**: If you use this Ansible role in your project, share your experiences, challenges, and solutions with the community. Your feedback can provide valuable insights and help others succeed with their projects.

Thank you for considering a contribution to the `ansible-role-setup-home-lab` project!

## Buy Me a Coffee ☕

If you find this project helpful and want to support its development, consider [buying me a coffee](https://www.buymeacoffee.com/your_username) to show your appreciation. Your support is greatly appreciated! 😊
