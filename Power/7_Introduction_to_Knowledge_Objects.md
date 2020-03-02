## What are Knowledge Objects?
- Knowledge objects are tools you use to discover and analyze various aspects of your data
    - Data interpretation
        - Fields and field extractions
    - Data classification
        - Event types
    - Data enrichment
        - Lookups and workflow actions
    - Normalization
        - Tags and field aliases
    - Datasets
        - Data models
- features
    - Shareable
    - Reusable
    - Searchable
## What is a knowledge manager?
- Oversees knowledge object creation and usage for a group or deployment
- Normalizes event data
- Creates data models for Pivot users
## Defining Naming Conventions
- Using a naming convention in your production environment is recommended
- Example is below
    - Group
    - Object Type
    - Description
    ```
    SEG_Alert_WinEventlogFailures
    ```
## Reviewing permissions
| case | Create | Read | Edit(write) |
| :---- | :------ | :---- | :----------- |
| private | User <br> Power <br> Admin | Person who created it <br> Admin | Person who created it <br> Admin |
| This app only | Power <br> Admin | User <br> Power <br> Admin | User <br> Power <br> Admin |
| App apps | Admin | User <br> Power <br> Admin | User <br> Power <br> Admin |

 