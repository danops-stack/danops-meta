# danops-meta

This PUBLIC repo stores some meta data and configuration for various danops tools.


# Deploy key
Some file(s) will be written automatically, e.g. by a CI pipeline. For such processes, a deploy key is used.

## Generate the key
The deploy key was generated as normal ssh key as follows:
```bash
ssh-keygen -t rsa -b 4096 -C "github.danops-stack.danops-metadata.deploykey1.c@danops"
  Enter file in which to save the key: /data/master/.ssh/danops_2020_github.danops-stack.danops-metadata.deploykey1_id_rsa
  Enter passphrase: (empty for no passphrase)
```

## Install the public deploy key in the GitHub repo
The public deploy key (content of public key file `danops_2020_github.danops-stack.danops-metadata.deploykey1_id_rsa.pub`) is added to this GitHub repo ('danops-metadata') under Settings/[Deploy keys](https://github.com/danops-stack/danops-metadata/settings/keys)/Add deploy key:
* Title: `danops_2020_github.danops-stack.danops-metadata.deploykey1_id_rsa.pub`
* Key: 
    ```
    ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQDKmo7XXPkny8lS2Hyc+GQFsd+2IRQVvuV62Xet8Fv8UIWIZ6AGrbwb4uOH5446B4TD+/egkgaTdewuC/REpmO1MPgHribSWuvwIPUCmyMSFqjRJfLhSr3pbTix8CJ/6vXAnr58VmLYlcRlfJeLofxI4D71nYwZFTH93WwurJkodOhm8YREzTQIjyVhrtWYOq5JV8iCrCjoGWL57LeVHZkvS3eU216vZbf7Z5UBeX3FoB6clRsXBPaBuRbGi+4I5NsAdOQ2cREl8gmLJaMoWFkvQjUCGuG5jBInRW2jRilJAvz9tTIntUe8RFrtK2/BlzKhd8t94sCwUNsD7cUFThIUo+EVWMHAh26msUTaF8kPuCeULcUhBJfkYmvNjiTKrbFo1HtpgrM8QOD8pUA7h+h3gLYopt8QKQJAjuOdYGgaV6s+94O9OKf2eRFqr47/js+zmXe31OJWDBB4lSpX5Do7OXDfajVeXzmmHMgHlvfidpRuiIkngCDWNQS6VJAUJyYJANfB/02430EFXc7TuYMmH7lStCgEjE94iXGISmdK2DDDSZ2bbxs6rs+lknL0cDtdrCtQhGd0BFzylClPajYCvglcieheLLUDnT/9DQ4PaxEN14S98kUBG7FZjVn+rcnzdY4d27pTW4pgOGIMa/HbwPZx2Ks80fH0HUCiKc9SBQ== github.danops-stack.danops-metadata.deploykey1.c@danops
    ``` 
* Allow write access: Yes

# Install the private deploy key in the CI pipeline environment
The private deploy key (content of public key file `danops_2020_github.danops-stack.danops-metadata.deploykey1_id_rsa`) is then added as base64 value (output of `cat danops_2020_github.danops-stack.danops-metadata.deploykey1_id_rsa | base64`) to an environment variable to the CI pipeline or to a variable inside `.circleci/config.yml`.

