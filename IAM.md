Notes:
Identity and Access Management (IAM) is a framework of policies and technologies for ensuring that the right individuals have the appropriate access to technology resources. IAM systems are critical to ensuring security and compliance, and they help organizations manage digital identities and control access to resources.
Key Components of IAM
• Identity Management - User Provisioning and Authentication
• Access Management - Authorization, RBAC, SSO
• Directory Services
• Policy Management
• Monitoring and Auditing - Logging and Reporting and Audit Trails

Que:
1.	What is AWS IAM?
    AWS IAM (Identity and Access Management) is a web service that helps you securely control access to AWS services and resources for your users. It enables you to create and manage AWS users and groups and use permissions to allow and deny their access to AWS resources.


2.	What are key features of IAM?
Key features of IAM include:
    •	Centralized control of AWS resources: IAM allows you to control who can use your AWS resources and what resources they can use.
    •	Granular permissions: You can create policies that define specific permissions for users, groups, and roles.
    •	Multi-factor authentication (MFA): IAM supports MFA for added security.
    •	Secure access to AWS resources for applications: IAM roles can be assigned to services like EC2 instances to grant temporary access to AWS resources.
    •	Identity federation: IAM allows you to manage user access to AWS resources using external identity providers.
    •	Integration with AWS services: IAM integrates with most AWS services to provide fine-grained access control.


3.	What is user and group in AWS IAM?
    •	User: An IAM user is an entity that you create in AWS to represent a person or service that interacts with AWS resources. Each user has unique credentials and can be assigned specific permissions using IAM policies.
    •	Group: An IAM group is a collection of IAM users. You can attach policies to groups, which makes it easier to manage permissions for multiple users. Users in a group inherit the permissions assigned to the group.


4.	What is Role and Policies in IAM?
    •	Role: An IAM role is an IAM identity that you can create in your account that has specific permissions. Roles are similar to users but are intended to be assumable by anyone who needs them, including applications, services, and other users. Roles are often used to grant permissions to applications running on EC2 instances or to allow cross-account access.
    •	Policies: IAM policies are JSON documents that define permissions to AWS resources. Policies specify what actions are allowed or denied and on which resources. Policies can be attached to users, groups, or roles to grant them the necessary permissions. There are several types of policies, including managed policies, inline policies, and service-control policies (SCPs).
