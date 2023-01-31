# Landing Zone on Demand

# Variables and secrets to define 

| Name | Type | Description | Specified In |
| ---- | ---- | ----------- | ------------ | 
| GH_User | Repo Variable  | Used to determine user to authenticate with.  Used in conjuction with 'GH_Token' variable | Core Repo |
| GH_Token | Repo Secret | Used to authenticate to GitHub to create repos/actions/etc... | Core Repo |
| GH_Org | Repo Variable | Used to determine the correct GitHub Org | Core Repo |
| TFC_TOKEN | Repo Secret | Used to authenticate with Terraform Cloud | Core Repo |
| TFC_AZURE_VAR_SET_NAME | Repo Variable | Used to identify the Variable Set in TFC to use to authenticate with Azure | Core Repo |
| ARM_SUBSCRIPTION_ID | Repo Secret | Used to specify the Azure subscription to authenticate with | ARM | Core Repo |



## Example command

### List GitHub Actions in a repository

```bash
pat='--- Enter your GitHub Personal Access Token ---'
org='--- Enter your GitHub Org name ---'
repo='--- Enter your GitHub Repo that contains the actions ---'

curl --request GET 'https://api.github.com/repos/$org/$repo/actions/workflows' \
--header "X-GitHub-Api-Version: 2022-11-28" \
--header "Accept: application/vnd.github+json" \
--header "Authorization: Bearer $pat" | jq '.workspaces'
```

