### Installation of Galaxy on Ilifu

This repo combines the setup of a Slurm submit host on the [Ilifu](https://ilifu.ac.za) with the installation of Galaxy and the configuration of Galaxy to submit to the Ilifu Slurm cluster. The Galaxy config is largely based on the [Galaxy Admin Training](https://training.galaxyproject.org/training-material/learning-pathways/admin-training.html) materials.

Galaxy is installed in `/ilifu/bio/projects/sanbi/pvh/galaxy`, a filesystem mounted using CephFS. The server runs as user `pvh`, which
is provided by LDAP. Singularity is largely used for tool dependency resolution.

In addition to the files in this repo, you need:

1. The Ansible roles as specified in `requirements.yml`.
2. The Vault password, saved in `.vault-password.txt`, that is in Bitwarden under the "galaxy-masters vault password" item.

The repo replaces the previous `masters_galaxy_ansible` repository.
