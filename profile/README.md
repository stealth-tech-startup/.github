I believe innovation is the strongest force that drives team in the right direction. My definition of innovation is

> My life gets changed dramatically in 2 hours

This org is dedicated for technologies that makes it happen

Quick Prototyping Tools
-----------------------

- [OpenStack Swift Docker Image](https://github.com/stealth-tech-startup/docker-swift-onlyone)
- [Cloudcraft](https://www.cloudcraft.co/)
- [TypeScript UML Playground](https://github.com/stealth-tech-startup/typescript-uml)
- [GraphQL server for fast prototyping](https://github.com/stealth-tech-startup/json-graphql-server)

<details><summary>Useful Shell Commands & Links</summary>

### Data Sourcing
  
- [Converting PDF to text](https://www.pdf2go.com/pdf-to-text)  
  
### Data Cleansing

- Filtering out lines **shorter** than 30 characters
  
  ```bash
  grep -E '^.{30,}$' input.txt > output.txt
  ```
 
</details>

Yahoo [Yavin](https://github.com/stealth-tech-startup/framework) - BI tool
--------------------------------------------------------------------------

We use Yavin internally to empower our data-based decision making

- [Documentation](https://stealth-tech-startup.github.io/yavin-docs/)
- [Example Yavin App (Template)](https://github.com/stealth-tech-startup/yavin-app)

  - [Externalized Config for the Example App (Template)](https://github.com/stealth-tech-startup/yavin-demo-config)

IaC via HashiCorp
-----------------

We used to love HashiCorp but we are now frustrated with its major mis-actions that hurt us as a country, including

- [Participating in the China-Ban](https://github.com/hashicorp/packer/pull/11888) (we know it's about government, but we don't care!)
- [Close-sourcing its techs, such as documentation](https://github.com/hashicorp/dev-portal/blob/main/docs/README.md):

  <img width="1005" alt="page" src="https://github.com/stealth-tech-startup/.github/assets/16126939/6e9e950e-b168-482e-a076-36398b43f624">

We predict that HashiCorp is going to keep shrinking its Open Source community and, thus, maintain a copy of what we depends here in case HashiCorp closes them:

- [HashiCorp Dev Portal](https://github.com/stealth-tech-startup/hashicorp-dev-portal)
- [HashiCorp Packer](https://github.com/stealth-tech-startup/hashicorp-packer)

  - [AWS Plugin](https://github.com/stealth-tech-startup/packer-plugin-amazon)

- [HashiCorp Terraform](https://github.com/stealth-tech-startup/hashicorp-terraform)
- [HashiCorp Vault](https://github.com/stealth-tech-startup/hashicorp-vault)
- [HashiCorp Vagrant](https://github.com/stealth-tech-startup/hashicorp-vagrant)
