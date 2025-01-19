# DEMO

- Setup pre-commit hook so that a commit message should always be mapped to JIRA 

1. Navigate to Git Hooks Directory
```
cd your-project/.git/hooks
```

2. Create or Edit the Pre-Commit Hook
Create a file named commit-msg if it doesn't exist:
```
touch commit-msg
chmod +x commit-msg
```

3. Add the Validation Script
Edit the commit-msg file:

```
vi commit-msg
```

Add the following script to enforce the JIRA ticket rule:

```
#!/bin/bash

# Extract commit message
COMMIT_MSG_FILE=$1
COMMIT_MSG=$(cat $COMMIT_MSG_FILE)

# Define a regex pattern for JIRA ticket format (e.g., SCRUM-123)
JIRA_REGEX="([A-Z]+-[0-9]+)"

# Check if the commit message contains a JIRA ticket
if [[ ! $COMMIT_MSG =~ $JIRA_REGEX ]]; then
  echo "❌ Commit message must include a JIRA ticket ID (e.g., SCRUM-123)."
  exit 1
fi

echo "✅ Commit message is valid."
```

4. Test the Hook
Try committing with and without a valid JIRA ticket ID in your message:

```
git commit -m "PROJECT-123: Fix login issue"
```
![image](https://github.com/user-attachments/assets/391419e4-72fd-4923-8938-78e483446aee)

```
git commit -m "Fix login issue"
```
![image](https://github.com/user-attachments/assets/e9bef36d-52dd-407c-b2c9-3aef51b7cb98)
