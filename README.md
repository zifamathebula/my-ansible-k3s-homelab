# my-ansible-k3s-homelab 🏡

An Ansible playbook to set up HA k8s cluster with k3s, kube-vip, MetalLB, ArgoCD via ansible within my homelab.

## Requirements 📋

- Ansible 2.9+ installed on the control machine
- SSH access to the target servers
- x1 Master Server running Ubuntu Server LTS 18.04+
- x1 Agent Server running Ubuntu Server LTS 18.04+
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/) installed on the control machine.
- A Slack workspace for receiving alerts (optional).

## Tooling 🧩

- Kube-vip:
- MetalLB: 
- Argo: App deployment

## Adding Apps 🚀

....

## Making changes 🧪

### Testing roles

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

Thank you for considering a contribution to the `my-ansible-k3s-homelab` project!

## Buy Me a Coffee ☕

If you find this project helpful and want to support its development, consider [buying me a coffee](https://www.buymeacoffee.com/zifamathebula) to show your appreciation. Your support is greatly appreciated! 😊
