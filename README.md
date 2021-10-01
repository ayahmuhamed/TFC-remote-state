# TFC-remote-state
Learn how to use terraform_remote_state with TFC remote backend


## Pre-requirements

* [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) 
* [Terraform cli](https://learn.hashicorp.com/tutorials/terraform/install-cli)
* [TFC account](http://app.terraform.io).
* [GitHub VCS provider configured in TFC](https://www.terraform.io/docs/cloud/vcs/github.html)

## How to use this repo

- Import ayahmuhamed/random_pet/random_pet repo in GitHub
- Create a new TFC workspace
- Clone this repo
- Cleanup

---

## Create a new Terraform Cloud workspace

* Create a new workspace in TFC, Version Control workflow, GitHub VCS and select your previously created repository

<img width="1261" alt="Screenshot 2021-10-01 at 14 36 01" src="https://user-images.githubusercontent.com/88331884/135620505-e85bdb8e-2ae5-4951-99fa-137f8d54f067.png">

<img width="1239" alt="Screenshot 2021-10-01 at 14 36 06" src="https://user-images.githubusercontent.com/88331884/135620560-4bafa86a-e1d0-48a0-b7d3-1e4fe0cf09f6.png">

<img width="1167" alt="Screenshot 2021-10-01 at 14 35 37" src="https://user-images.githubusercontent.com/88331884/135620630-7a3b15f7-c1f3-4f05-b000-52fca5731792.png">


* Queue a plan and apply


<img width="1607" alt="Screenshot 2021-10-01 at 10 40 57" src="https://user-images.githubusercontent.com/88331884/135620816-ed202899-6389-40be-bcd2-7bb029959946.png">


### Clone the repo

```
git clone https://github.com/ayahmuhamed/TFC-remote-state
```

### Change directory

```
cd TFC-remote-state
```

### Update main.tf

In the main.tf update the below content with your previously created TFC workspace details

```
  config = {
    organization = "YOUR-ORGANIZATION-NAME"
    workspaces = {
      name = "YOUR-WORKSPACE-NAME"
    }
  }
}
```

### Run

* Init:

```
terraform init
```



* Apply:

```
terraform apply
```

