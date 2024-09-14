<!--suppress HtmlUnknownAnchorTarget -->
<div style="text-align: center;" class="myWrapper">

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

</div>

<!-- PROJECT LOGO -->
<br />
<div align="center">

  [![logo](images/logo.svg)](https://github.com/DanielJShen/nginx-reverse-proxy)

  <h2 align="center">NGINX Reverse Proxy</h2>

  <div align="center">
    <p>A custom NGINX Reverse Proxy installable on an AWS EC2 container using Terraform</p>
    <p>
      <a href="https://github.com/DanielJShen/nginx-reverse-proxy/issues/new?labels=bug&template=bug-report---.md">Report Bug</a>
      ·
      <a href="https://github.com/DanielJShen/nginx-reverse-proxy/issues/new?labels=enhancement&template=feature-request---.md">Request Feature</a>
    </p>
  </div>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About The Project

This project contains an NGINX Reverse Proxy and the tools for installing it on an AWS EC2 container.

The Reverse Proxy is specifically designed to:

- Increase the security of a HTTPS server
    - Block unexpected requests
    - Block IPs based on suspicious activity
- Cache frequently requested content
- Perform SSL encryption on behalf of the server

#### Built With

[![Terraform][terraform]][terraform-url]
[![nginx][nginx]][nginx-url]

<!-- GETTING STARTED -->
## Getting Started

Below are the steps to use this project to create an AWS EC2 container running an NGINX Reverse Proxy. 

### Prerequisites

1. Install Terraform using the following guide: [Terraform Docs - Install CLI](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)

### Installation

1. Clone this repo
   ```sh
   git clone https://github.com/DanielJShen/nginx-reverse-proxy.git
   ```
2. Update the configuration file with the following steps:
    1. Set the EC2 instance id/keys
3. Run these command and ensure they run successfully: 
   1. `terraform init`
   2. `terraform validate`

<!-- USAGE EXAMPLES -->
## Usage

To create the ec2 instance you can run the following command:

`AWS_ACCESS_KEY_ID=<KEY_ID> AWS_SECRET_ACCESS_KEY=<KEY> terraform apply`

It will take the provided AWS Access Key and then create a `t2.micro` instance in the `eu-west-2` region.
These values can be changed in `terraform/config.yaml`

<!-- ROADMAP -->
## Roadmap

- [ ] Add Changelog
- [ ] Add Terraform config
- [ ] Add NGINX config
- [ ] Update README
- [ ] Add more useful NGINX config 

See the [open issues](https://github.com/DanielJShen/nginx-reverse-proxy/issues) for a full list of proposed features (and known issues).

<!-- CONTRIBUTING -->
## Contributing

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Top contributors:

<a href="https://github.com/DanielJShen/nginx-reverse-proxy/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=DanielJShen/nginx-reverse-proxy" alt="Contributors" />
</a>

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* Choose an Open Source License
  * https://choosealicense.com
* Best-README-Template
  * [![Best_README_Template](https://img.shields.io/badge/Best_README_Template-black?style=plastic&logo=github&logoColor=white)](https://github.com/othneildrew/Best-README-Template)

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/DanielJShen/nginx-reverse-proxy.svg?style=for-the-badge
[contributors-url]: https://github.com/DanielJShen/nginx-reverse-proxy/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/DanielJShen/nginx-reverse-proxy.svg?style=for-the-badge
[forks-url]: https://github.com/DanielJShen/nginx-reverse-proxy/network/members
[stars-shield]: https://img.shields.io/github/stars/DanielJShen/nginx-reverse-proxy.svg?style=for-the-badge
[stars-url]: https://github.com/DanielJShen/nginx-reverse-proxy/stargazers
[issues-shield]: https://img.shields.io/github/issues/DanielJShen/nginx-reverse-proxy.svg?style=for-the-badge
[issues-url]: https://github.com/DanielJShen/nginx-reverse-proxy/issues
[license-shield]: https://img.shields.io/github/license/DanielJShen/nginx-reverse-proxy.svg?style=for-the-badge
[license-url]: https://github.com/DanielJShen/nginx-reverse-proxy/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://uk.linkedin.com/in/danieljshenfield
[terraform]: https://img.shields.io/badge/Terraform-EFEFEF?style=for-the-badge&logo=terraform&logoColor=purple
[terraform-url]: https://www.terraform.io/
[nginx]: https://img.shields.io/badge/NGINX-black?style=for-the-badge&logo=nginx&logoColor=green
[nginx-url]: https://github.com/nginx/njs/
