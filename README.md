# aws-operation
Documents for Amazon Web Service Operation
## File IP Config
```
declare -x Dev="174.789.78.0"
declare -x Stage="174.789.78.1"
declare -x Pro="174.789.78.2"
```
## Get Export From File IP Config
```
source filename
```
## How To Run Multiple SSH Command
```
cat remote-box-commands.bash | ssh -t server
```
