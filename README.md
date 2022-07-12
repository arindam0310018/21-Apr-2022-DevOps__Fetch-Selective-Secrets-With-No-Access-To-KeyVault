# FETCH SELECTIVE SECRETS WITH NO ACCESS TO KEY VAULT USING DEVOPS PIPELINES

Greetings my fellow Technology Advocates and Specialists!!!

This Blog post is a follow-up to **<u>my previous post</u>** - [Fetch Secrets with no access to key vault] (https://dev.to/arindam0310018/fetch-secrets-with-no-access-to-key-vault-using-devops-pipelines-54h3)

| **MY SUGGESTION:-** | 
| --------- |
| Please Read my previous blog first to better understand the Use Case |

| **USE CASES:-** | 
| --------- |
| Fetch Secrets only with Tags (any) |
| Fetch Secrets only with Specific defined Tags |

| __LIVE RECORDED SESSION:-__ |
| --------- |
| __LIVE DEMO__ was Recorded as part of my Presentation in __WELSH AZURE GROUP__ Forum/Platform |
| Duration of My Demo = __32 Mins 38 Secs__ |
| Start and End Time = __00:39:22 to 01:12:00__ |

| [![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/um_6WtIBSA8/0.jpg)](https://www.youtube.com/watch?v=um_6WtIBSA8) |
| --------- |

| __REQUIREMENTS:-__ |
| --------- |

1. Azure Key Vault
2. Four Sample Secrets in Azure Key Vault
3. Add Tags to One or More Secrets 
4. Azure Resource Manager Service Connection 
5. Azure DevOps Pipeline (YAML)

| **NOTE:-** |
| --------- |

The Service Principal (which is required to Create Service Connection) should at minimum have **GET** and **LIST** Access Policy Permissions in Azure Key Vault.

| __BELOW DISPLAYS THE SAMPLE SECRETS IN KEY VAULT:-__ |
| --------- |
| ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/npsfbj72ds452270pbmk.png)  |

| __WHERE DO WE APPLY TAGS IN KEY VAULT SECRET:-__ |
| --------- |
| ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/myl91y0jliypmxvjx6dt.png) |
| ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/kendex7v7zg3e6kk8vqy.png) |

| __BELOW DISPLAYS THE SECRET TAGS IN KEY VAULT:-__ |
| --------- |

| NAME OF THE SECRET | TAGS ASSOCIATED WITH SECRET |
| --------- | --------- |
| AMSecret005 | ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/0fjqve09z2qxhb2d96ei.png) |
| AMSecret006 | ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/cq2mqytunhw7bl3zxwwe.png) |
| AMSecret007 | No Tags Configured |
| AMSecret008 | ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/0fjqve09z2qxhb2d96ei.png) |

| # | PIPELINE TASKS | 
| --------- | --------- |
| 1. | AZURE KEY VAULT TASKS |
| 2. | FETCH **ALL SECRETS WITH TAGS** OR **ALL SECRETS WITH SPECIFIC TAG**. EXPORT IT THEN IN A TEXT FILE | 
| 3. | COPY THE SECRETS TEXT FILE TO ARTIFACTS STAGING DIRECTORY |
| 4. | PUBLISH THE ARTIFACTS |
