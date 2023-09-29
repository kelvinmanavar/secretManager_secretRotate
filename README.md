# secretManager_secretRotate
I will write a code for lambda function for rotating secrets
# update lambda_function.py
Edit 
current_secrets.update({
        "KEY_TO_ROTATE" : newPassword
    })
Replace KEY_TO_ROTATE with your original identified key word like password.

Replace SecretId with your secret manager secret name.

# Update policy.json
Replace secretARN from your secret manager ARN.

# Setup lambda function:
	# Modify Role in lambda function:
	Add inline policy from policy.json
	# create Resource-based policy statements in lambda configuration.
		# Select AWS Service
		# Give any statement id like sample-id.
		# Select Action: lambda:invokeFunction.
# Secret Manager:
	# Secret Type select other type of secret.[as per requirement].
	# select key-value pair.
	# Give secret name.
	# Select Automatic rotation.
	# Select Lambda rotation function.

