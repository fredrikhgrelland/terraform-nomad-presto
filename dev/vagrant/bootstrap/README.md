# Customize the startup procedure of the Hashistack with pre- and post start ansible scripts

You may put any number of script files in this directory for running ansible commands prior to bootstrapping the hashistack.
The bootstrap procedure is included/hardcoded in your box.
[bootstrap.yml](https://github.com/skatteetaten/vagrant-hashistack/blob/master/ansible/bootstrap.yml) will start by running the scripts in this folder and end by running the scripts in [../post_bootstrap](../post_bootstrap)


The files e.g. 0-example.yml must only include pure ansible task syntax:
```yaml
- name: Task that shows usage of prestart
  debug:
    msg: This would be a prestart task
```

See [example](https://github.com/Skatteetaten/vagrant-hashistack-template/blob/master/template_example/dev/vagrant/bootstrap/consul/pre/510-prestart-example.yml)
