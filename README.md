# employee-data-app

$ACCOUNT = aws sts get-caller-identity --query Account --output text --profile employee-lab

# Lambda: zip the folder and replace the placeholder

Compress-Archive -Path lambda\* -DestinationPath function.zip -Force
aws lambda update-function-code --function-name employee-data-shyamkumar-export --zip-file fileb://function.zip --profile employee-lab