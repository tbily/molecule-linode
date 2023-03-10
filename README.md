# molecule-linode
Molecule driver for Linode

Based on [molecule-digitalocean](https://github.com/ansible-community/molecule-digitalocean) 

Allows using Linode for testing roles. 

Requires ```LINODE_ACCESS_TOKEN``` environment variable defined to provision the nodes. 
You will need community.general collection:

```
ansible-galaxy collection install community.general
```

Please note this is not officially supported plugin and needs modifying defult list of available plugins in molecule:

```
molecule/data/molecule.json
```

```
"MoleculeDriverModel": {
      "additionalProperties": false,
      "properties": {
        "cachier": {
          "title": "Cachier",
          "type": "string"
        },
        "default_box": {
          "title": "DefaultBox",
          "type": "string"
        },
        "name": {
          "enum": [
            "azure",
            "ec2",
            "delegated",
            "docker",
            "containers",
            "openstack",
            "podman",
            "vagrant",
            "digitalocean",
            "gce",
            "libvirt",
            "lxd",
            "linode"
          ],
```
