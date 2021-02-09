# packer-plugin-vmware-ova
A plugin for HashiCorp's Packer.
This plugin provides a builder that imports an `ova` file and exports the same `ovf`
properties in the exported `ova` file. It's also possible to provide additional `ovf` properties.
Additionally, this plugin provides a post-processor that allows to upload the `ova` to a vSphere Content Library.

The idea behind the output of this plugin's post-processor is to use the accompanying
[Terraform module](https://github.com/artpropp/terraform-vsphere-content-library), which is just a thin wrapper around the 
official `Terraform vSphere` provider.
If you don't want to use an additional tool such as Terraform, you can use the  official `vSphere` post-processor
bundled with Packer to deploy your freshly built ova file.

The builder in this plugin runs locally on VMware Workstation (for Linux and Windows), VMware Fusion (for macOS),
or VMware Player (on Linux). It also runs on Vmware vSphere

## How to install
Follow the same installation instructions as described in the
[Packer documentation](https://www.packer.io/docs/extending/plugins#installing-plugins).


## Build from source