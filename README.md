# To  hiding your credentials securely or working with environment variables!

## Option 1 
-Step 1 Set environment variables
    -   In your terminal, set them like this (temporary for that shell):

```bash
export DB_USER=jusgowiturs
export DB_PASS='*************'// Replace * with you passcode
export DB_HOST=localhost
export DB_NAME=testdb
```
-   On Windows Command Prompt:

```ini
set DB_USER=jusgowiturs
set DB_PASS=*************// Replace * with you passcode
set DB_HOST=localhost
set DB_NAME=testdb
```
-   Step 2 To Access in python
```python
import os
# Read credentials from environment variables
user = os.getenv('DB_USER')
password = os.getenv('DB_PASS')
host = os.getenv('DB_HOST')
db = os.getenv('DB_NAME')
```
## Option 2 Use .env file(Projects this is a good method)
-   Create a .env file in your project folder:
```ini
DB_USER=jusgowiturs
DB_PASS=*************// Replace * with you passcode
DB_HOST=localhost
DB_NAME=testdb
```
-   Install python-dotenv
```bash
pip install python-dotenv
```
-   Load .env in Python:
-   Using load_dotenv() and os.getenv() together is actually the standard and recommended pattern when you want to load environment variables from a .env file into your Python environment.
```python
from dotenv import load_dotenv
import os

# Load variables from .env
load_dotenv()

user = os.getenv('DB_USER')
password = os.getenv('DB_PASS')
host = os.getenv('DB_HOST')
db = os.getenv('DB_NAME')
```

