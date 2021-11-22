*Context: InfoSec identified a security incident related to the leakage of AWS credentials. The context of the leaked key may or may not be known. An Incident Lead, determined by InfoSec, is applying the steps below to guarantee that the attack is either contained or prevented.*

## Procedures for managing AWS access keys:

1. **Communicate** to the applicable stakeholders.
2. **Locate** the IAM admin **in order to provide** AWS permissions removal from affected users **without** revoking credentials.  
`tbd sec iam show group infosec-permissions-admin`
3. **Ask to remove** all inline policies from the **IAM** users affected.  
`tbd iam disallow <user> Source`  
4. Ask the admin **to reach out and communicate** the affected users about their immediate removal from respective IAM groups.  
`tdb sec iam show <user>`  
`tbd sec iam remove <user> <group>`  
5. **Send a message** to the affected users:  
*"Hi, we hope to find you well. The reason for our contact is to inform you about a possible security incident already under our investigation.  To protect your security we have temporarily suspended your AWS permissions. We kindly ask you to keep this incident private until a solution. If you have any questions, please get in touch with our support team. Thank you."*  
6. Ask **to revoke** the affected credentials and **generate new** ones and key pairs using the AWS console.