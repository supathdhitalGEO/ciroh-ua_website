---
sidebar_position: 2
title: "Tag Resources on AWS"
description: "AWS tags for cost tracking"
tags:
  - AWS
  - Tag
  - Cost
---

import useBaseUrl from '@docusaurus/useBaseUrl'

Tags in AWS are essential for organizing resources based on their purpose, owner, or environment, and can also aid in cost tracking when unique key-value pairs are assigned.

# How to Tag Resources on AWS

1. Using AWS Console:

Navigate to the desired resource, such as an EC2 instance, and follow these steps:

- Select the instance from the list view.
- Go to the Tags tab and click on the Manage tags button.
- Add a new tag with a unique Key and Value.
  
<p align="center">
<img src={useBaseUrl("/img/EC2-CreateTag.png")} alt="AWS 'manage tags' window" style={{'width':'50%', 'height':'50%'}}/>
</p>

- Save the changes.

2. Using AWS CLI:

Use the following command-line example to create a tag for an EC2 instance:
  ```
  aws ec2 create-tags \
    --resources i-1234567890abcdef0 \
    --tags Key=webserver,Value=dev
  ```

For each project, tag all its resources with:

Project=project_name (e.g., ciroh-hydroshare, ciroh-fim)
Double-check the tag name with the AWS main account admin to make sure it fits well with our naming scheme.
