# Landing Zone on Demand

# Variables and secrets to define 

| Name | Type | Description | Specified In |
| ---- | ---- | ----------- | ------------ | 
| GH_User | Repo Variable  | Used to determine user to authenticate with.  Used in conjuction with 'GH_Token' variable | Core Repo |
| GH_Token | Repo Secret | Used to authenticate to GitHub to create repos/actions/etc... | Core Repo |
| GH_Org | Repo Variable | Used to determine the correct GitHub Org | Core Repo |
