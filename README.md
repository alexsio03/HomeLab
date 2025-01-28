
# Alex's Homelab

## Overview

Project status: **ALPHA**

This project is still in the beginning stages. I will be **SLOWLY** adding to this repository, as I want to be sure I don't accidentally add any keys or screts that should not go to the public.

### Hardware

![Hardware](https://github.com/user-attachments/assets/c12e54f0-586d-4770-8dcc-8bb4c84d3e26)


- 3 × Lenovo ThinkCentre `M900 USFF`:
    - CPU: `Intel Core i5-4570T`
    - RAM: `4GB`
    - SSD: `512GB`
- TP-Link `TL-SG105` switch:
    - Ports: `5`
    - Speed: `1000Mbps`

### Features

- [x] Common applications: Gitea, Jellyfin, Paperless...
- [x] Automated Kubernetes installation and management
- [x] Automatic rolling upgrade for OS and Kubernetes
- [x] Automatically update apps (with approval)
- [x] Modular architecture, easy to add or remove features/components
- [x] Automated certificate management
- [x] Automatically update DNS records for exposed services
- [x] VPN (Tailscale or Wireguard)
- [x] Expose services to the internet securely with [Cloudflare Tunnel](https://www.cloudflare.com/products/tunnel/)
- [x] Private container registry
- [x] Distributed storage
- [x] Monitoring and alerting
- [x] Automated backup and restore
- [x] Single sign-on
- [x] Infrastructure testing

Some demo videos and screenshots are shown here.
They can't capture all the project's features, but they are sufficient to get a concept of it.

| Current Services                                                                                                |
| :--:                                                                                                            |
| [![][rancher]][rancher]                                                                                         |
| Cluster/Node management UI in Rancher                                                                           |
| [![][longhorn]][longhorn]                                                                                       |
| Distributed storage across nodes in LongHorn                                                                    |
| [![][traefik]][traefik]                                                                                         |
| Network access point monitoring and notifications with Traefik                                                  |
| [![][homepage]][homepage]                                                                                       |
| Homepage for quick access and hyperlinks to tools                                                               |
| [![][gitea]][gitea]                                                                                             |
| Locally hosted Git service for private repositories                                                             |

[rancher]: https://github.com/user-attachments/assets/14fabeb7-8566-491c-9b54-4e69107e0ab7
[traefik]: https://github.com/user-attachments/assets/c6ad0ce2-71e0-4a5e-a257-3264cce4485f
[longhorn]: https://github.com/user-attachments/assets/787d407d-d822-4e1d-bb93-cabadc7d1934
[homepage]: https://github.com/user-attachments/assets/1501cb19-0d3b-4fbe-bb74-05a70b0657c0
[gitea]: https://github.com/user-attachments/assets/11a1554e-7490-4bfd-b0df-a50aa48c902b

### Tech stack

<table>
    <tr>
        <th>Logo</th>
        <th>Name</th>
        <th>Description</th>
    </tr>
    <tr>
        <td><img width="32" src="https://simpleicons.org/icons/ansible.svg"></td>
        <td><a href="https://www.ansible.com">Ansible</a></td>
        <td>Automate bare metal provisioning and configuration</td>
    </tr>
    <tr>
        <td><img width="32" src="https://github.com/jetstack/cert-manager/raw/master/logo/logo.png"></td>
        <td><a href="https://cert-manager.io">cert-manager</a></td>
        <td>Cloud native certificate management</td>
    </tr>
    <tr>
        <td><img width="32" src="https://avatars.githubusercontent.com/u/314135?s=200&v=4"></td>
        <td><a href="https://www.cloudflare.com">Cloudflare</a></td>
        <td>DNS and Tunnel</td>
    </tr>
    <tr>
        <td><img width="32" src="https://www.docker.com/wp-content/uploads/2022/03/Moby-logo.png"></td>
        <td><a href="https://www.docker.com">Docker</a></td>
        <td>Ephemeral PXE server</td>
    </tr>
     <tr>
        <td><img width="32" src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4a/Debian-OpenLogo.svg/200px-Debian-OpenLogo.svg.png"></td>
        <td><a href="https://getfedora.org/en/server">Debian</a></td>
        <td>Base OS for Kubernetes nodes</td>
    </tr>
    <tr>
        <td><img width="32" src="https://helm.sh/img/helm.svg"></td>
        <td><a href="https://helm.sh">Helm</a></td>
        <td>The package manager for Kubernetes</td>
    </tr>
    <tr>
        <td><img width="32" src="https://avatars.githubusercontent.com/u/49319725"></td>
        <td><a href="https://k3s.io">K3s</a></td>
        <td>Lightweight distribution of Kubernetes</td>
    </tr>
    <tr>
        <td><img width="32" src="https://avatars.githubusercontent.com/u/13629408"></td>
        <td><a href="https://kubernetes.io">Kubernetes</a></td>
        <td>Container-orchestration system, the backbone of this project</td>
    </tr>
     <tr>
        <td><img width="32" src="https://avatars.githubusercontent.com/u/1412239?s=200&v=4"></td>
        <td><a href="https://www.nginx.com">NGINX</a></td>
        <td>Kubernetes Ingress Controller</td>
    </tr>
    <tr>
        <td><img width="32" src="https://avatars.githubusercontent.com/u/48932923?s=200&v=4"></td>
        <td><a href="https://tailscale.com">Tailscale</a></td>
        <td>VPN without port forwarding</td>
    </tr>
    <tr>
        <td><img width="32" src="https://avatars.githubusercontent.com/u/13991055?s=200&v=4"></td>
        <td><a href="https://www.wireguard.com">Wireguard</a></td>
        <td>Fast, modern, secure VPN tunnel</td>
    </tr>
    <tr>
        <td><img width="32" src="https://metallb.io/images/logo/metallb-white.png"></td>
        <td><a href="https://metallb.io/">MetalLB</a></td>
        <td>Load-balancer implementation for bare metal Kubernetes clusters</td>
    </tr>
    <tr>
        <td><img width="32" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSngjP80gSN2OViqOtEWiQk8Fkvf4TPcMh9_w&s"></td>
        <td><a href="https://www.rancher.com">Rancher</a></td>
        <td>Open-source platform for Kubernetes management</td>
    </tr>
    <tr>
        <td><img width="32" src="https://longhorn.io/img/logos/longhorn-icon-white.png"></td>
        <td><a href="https://longhorn.io/">LongHorn</a></td>
        <td>Cloud native distributed block storage for Kubernetes</td>
    </tr>
    <tr>
        <td><img width="32" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR5TgvfyQXTfJo_XdQc6eP0GLWYev0JaMrhAQ&s"></td>
        <td><a href="https://traefik.io/traefik/">Traefik</a></td>
        <td>Open source reverse proxy and ingress controller</td>
    </tr>
    <tr>
        <td><img width="32" src="https://avatars.githubusercontent.com/u/10625446?s=280&v=4"></td>
        <td><a href="https://ngrok.com/">Ngrok</a></td>
        <td>TCP Gateway for MC server</td>
    </tr>
    <tr>
        <td><img width="32" src="https://upload.wikimedia.org/wikipedia/commons/b/bb/Gitea_Logo.svg"></td>
        <td><a href="https://gitea.com">Gitea</a></td>
        <td>Self-hosted Git service</td>
    </tr>
    <tr>
        <td><img width="32" src="https://github.com/user-attachments/assets/7ace3c45-655d-4ec8-80c9-c917724693b8"></td>
        <td><a href="https://gethomepage.dev/">Homepage</a></td>
        <td>Self-hosted dashboard with hyperlinks and tools</td>
    </tr>
</table>

## License

Copyright &copy; 2024 - 2025 Alex Warda

## Acknowledgements

References:

- [README template](https://github.com/khuedoan/homelab/blob/master/README.md)

