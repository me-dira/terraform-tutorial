# Devops Hobbies Terraform Tutorial

<a href=""><img style="max-width: 900px; width: 100%" src="./assets/thumbnail.jpg"></a>

This is brand new Persian Terraform free tutorial from @[babakDoraniArab](https://github.com/babakDoraniArab),
contribute and improve this tutorial repo.

## Table of Contents

1. [Terraform Installation](#installation)
2. [Extensions](#extensions)
3. [About Course](#about-course)

## Installation

You can find your os related help for installation in below:

<details >
<summary > Linux </summary>

<ul>
    
<details>
<summary> Debian/Ubuntu </summary>
    
#### Ubuntu/Debian
Ensure that your system is up to date and you have installed the gnupg, software-properties-common, and curl packages installed. You will use these  packages to verify HashiCorp's GPG signature and install HashiCorp's Debian package repository.
  
```bash
sudo apt-get update && sudo apt-get install -y gnupg software-properties-common
```
Install the HashiCorp GPG key.
```bash
wget -O- https://apt.releases.hashicorp.com/gpg | \
  gpg --dearmor | \
  sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg
```
Verify the key's fingerprint.
```bash
   gpg --no-default-keyring \
    --keyring /usr/share/keyrings/hashicorp-archive-keyring.gpg \
    --fingerprint
```
The gpg command will report the key fingerprint:
```
    /usr/share/keyrings/hashicorp-archive-keyring.gpg
    -------------------------------------------------
    pub   rsa4096 XXXX-XX-XX [SC]
          AAAA AAAA AAAA AAAA
    uid           [ unknown] HashiCorp Security (HashiCorp Package Signing) <security+packaging@hashicorp.com>
    sub   rsa4096 XXXX-XX-XX [E]
```
  Add the official HashiCorp repository to your system. The lsb_release -cs command finds the distribution release codename for your current system, such as buster, groovy, or sid.
  ```bash
  echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] \
    https://apt.releases.hashicorp.com $(lsb_release -cs) main" | \
    sudo tee /etc/apt/sources.list.d/hashicorp.list
  ```
   Download the package information from HashiCorp.
   ```bash
   sudo apt update
   ```
   Install Terraform from the new repository.
   ```bash
   sudo apt-get install terraform
   ```

</details>

<details>
<summary> CentOS/RHEL </summary>

Install yum-config-manager to manage your repositories.

```bash
sudo yum install -y yum-utils
```

Use yum-config-manager to add the official HashiCorp Linux repository.

```bash
sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/RHEL/hashicorp.repo
```

Install Terraform from the new repository.

```bash
sudo yum -y install terraform
```

</details>
</li>

<details>
<summary>Fedora</summary>

### Fedora

Install `dnf config-manager` to manage your repositories.

```bash
sudo dnf install -y dnf-plugins-core
```

Use `dnf config-manager` to add the official HashiCorp Linux repository.

```bash
sudo dnf config-manager --add-repo https://rpm.releases.hashicorp.com/fedora/hashicorp.repo
```

Install Terraform from the new repository.

```bash
sudo dnf -y install terraform
```

</details>

<details>
<summary> Amazon-linux </summary>

Install yum-config-manager to manage your repositories.

```bash
sudo yum install -y yum-utils
```

Use yum-config-manager to add the official HashiCorp Linux repository.

```bash
sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/AmazonLinux/hashicorp.repo
```

Install Terraform from the new repository.

```bash
sudo yum -y install terraform
```

</details>
</ul>
</details>

<details>
<summary> Mac and Windows </summary>

<ul>
<details>
<summary> Homebrew OS X </summary>

First, install the HashiCorp tap, a repository of all our Homebrew packages.

```bash
brew tap hashicorp/tap
```

Now, install Terraform with hashicorp/tap/terraform.

```bash
brew install hashicorp/tap/terraform
```

To update to the latest version of Terraform, first update Homebrew.

```bash
brew update
```

Then, run the upgrade command to download and use the latest Terraform version.

```bash
brew upgrade hashicorp/tap/terraform
```

</details>

<details>
<summary> Chocolatey on Windows </summary>

Chocolatey is a free and open-source package management system for Windows. Install the Terraform package from the command-line.

```cmd
choco install terraform
```

</details>

</ul>

</details>

<details>
<summary> Manual </summary>

To install Terraform, find the [appropriate package](https://developer.hashicorp.com/terraform/downloads) for your system and download it as a zip archive.

After downloading Terraform, unzip the package. Terraform runs as a single binary named `terraform`. Any other files in the package can be safely removed and Terraform will still function.

Finally, make sure that the `terraform` binary is available on your `PATH`. This process will differ depending on your operating system.

<ul>
<details>
<summary> Mac or Linux </summary>

Print a colon-separated list of locations in your PATH.

```bash
echo $PATH
```

Move the Terraform binary to one of the listed locations. This command assumes that the binary is currently in your downloads folder and that your `PATH` includes `/usr/local/bin`, but you can customize it if your locations are different.

```bash
mv ~/Downloads/terraform /usr/local/bin/
```

For more detail about adding binaries to your path, see this [Stack Overflow article](https://stackoverflow.com/questions/14637979/how-to-permanently-set-path-on-linux).

</details>

<details>
<summary> Windows </summary>

[This Stack Overflow article](https://stackoverflow.com/questions/1618280/where-can-i-set-path-to-make-exe-on-windows) contains instructions for setting the PATH on Windows through the user interface.

</details>
</ul>
</details>

## Extensions

Effective programming with TLS (Terraform Language Server) to have syntax highlighting, intellisense, code formatting and etc.

| Name                                                                                        | Description                                                                                                                                      |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| [VsCode extension](https://marketplace.visualstudio.com/items?itemName=hashicorp.terraform) | Terraform Extension for Visual Studio Code                                                                                                       |
| [LSP Mode](https://emacs-lsp.github.io/lsp-mode/page/lsp-terraform-ls/)                     | Aims to provide IDE-like experience by providing optional integration with the most popular Emacs packages like company, flycheck and projectile |

## About Course

Leave a star on this repository and then subscribe to our [Youtube](https://www.youtube.com/@devopshobbies) channel. Be aware to turn on notification bell to get notified in case new video added.

Every episode codes are pushed to its related branch and you can check them below.

| Episode | Name                                                                       | branch                                                               | Youtube                               |
| ------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------- | ------------------------------------- |
| 001     | Introduction                                                               | -                                                                    | [watch](https://youtu.be/aFk04rQWvOM) |
| 002     | Why LaC                                                                    | -                                                                    | [watch](https://youtu.be/Ta-gJecexlg) |
| 003     | Configuration management vs infrastructure orchestration                   | -                                                                    | [watch](https://youtu.be/n_DckVP5nJQ) |
| 004     | Terraform Providers and basic AWS configuration to get programmatic access | [004](https://github.com/devopshobbies/terraform-tutorial/tree/v004) | [watch](https://youtu.be/KFg3jDemBF4) |
| 005     | Create your first resource with terraform                                  | [005](https://github.com/devopshobbies/terraform-tutorial/tree/v005) | [watch](https://youtu.be/tM8eNLZTfKg) |
| 006     | How to edit your resource and destroy your project                         | [006](https://github.com/devopshobbies/terraform-tutorial/tree/v006) | [watch](https://youtu.be/ugP6cx2jibI) |
| 007     | Terraform variables and terraform variables                                | [007](https://github.com/devopshobbies/terraform-tutorial/tree/v007) | [watch](https://youtu.be/BOZZzbv1ubc) |
| 008     | Terraform variables and terraform variables                                | [008](https://github.com/devopshobbies/terraform-tutorial/tree/v008) | [watch](https://youtu.be/RV3OkiYKojk) |
| 009     | Terraform remote backend                                                   | [009](https://github.com/devopshobbies/terraform-tutorial/tree/v009) | [watch](https://youtu.be/yZQdhRil6TM) |
| 010     | terraform import and state rm                                              | [010](https://github.com/devopshobbies/terraform-tutorial/tree/v010) | [watch](https://youtu.be/CBHYhMlq6Qc) |
